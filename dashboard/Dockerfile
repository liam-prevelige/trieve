# Using a multi-stage build to separate dependency analysis from the production environment
FROM node:18 as build

WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN yarn install

# Install Graphviz
RUN apt-get update && apt-get install -y graphviz

# Copy the rest of your application source code
COPY . .

# Build the application
RUN yarn run build

# Install madge, a tool to analyze and visualize module dependencies
RUN yarn add madge

# Generate dependency graph for TypeScript files
RUN npx madge --image graph.svg src/

# Production image using Nginx to serve the built application
FROM nginx:1.25.4-alpine-slim

WORKDIR /usr/share/nginx/html

# Copy the built application from the build stage
COPY --from=build /app/dist /usr/share/nginx/html

# Copy the dependency graph into a known directory (e.g., for access via a specific URL)
COPY --from=build /app/graph.svg /usr/share/nginx/html/graph.svg

# Standard Nginx configuration
COPY <<'EOF' /etc/nginx/conf.d/default.conf
server {
    listen 80;

    root /usr/share/nginx/html;
    index index.html;

    location / {
        try_files $uri $uri/ /index.html;
    }

    # Optionally serve the dependency graph at a specific route
    location /deps {
        alias /usr/share/nginx/html/graph.svg;
    }
}
EOF

# Script to manage environment variables and dynamic config generation
COPY <<'EOF' /docker-entrypoint.d/01-insert-window-variable.sh
#!/bin/sh

set -eu

cp /usr/share/nginx/html/index.html /usr/share/nginx/html/index.html.template
envsubst < /usr/share/nginx/html/index.html.template > /usr/share/nginx/html/index.html 
rm /usr/share/nginx/html/index.html.template

EOF

RUN chmod +x /docker-entrypoint.d/01-insert-window-variable.sh

EXPOSE 80
