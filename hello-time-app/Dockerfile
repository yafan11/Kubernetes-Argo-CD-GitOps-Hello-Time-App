# Use official NGINX 1.26.3-alpine base image
FROM nginx:1.26.3-alpine

# Delete default server configuration
RUN rm /etc/nginx/conf.d/default.conf

# Copy hello-time-app server configuration file
COPY hello-time-app.conf /etc/nginx/conf.d/

# Copy hello-time-app web page into the default root directory
COPY index.html /usr/share/nginx/html/

# Expose NGINX port
EXPOSE 80
