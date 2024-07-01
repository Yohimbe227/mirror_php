FROM debian:bookworm-slim

# Install Nginx and the required modules
RUN apt-get update && apt-get install -y \
    nginx \
    nginx-full \
    libnginx-mod-http-auth-pam \
    libnginx-mod-http-dav-ext \
    libnginx-mod-http-echo \
    libnginx-mod-http-geoip2 \
    libnginx-mod-http-subs-filter \
    libnginx-mod-http-upstream-fair \
    libnginx-mod-stream-geoip2 \
    && apt-get clean

# Clean up APT when done
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Copy Nginx configuration files if needed
# COPY nginx.conf /etc/nginx/nginx.conf
# COPY fastcgi-php.conf /etc/nginx/snippets/fastcgi-php.conf

# Expose ports
EXPOSE 80 443

# Start nginx
CMD ["nginx", "-g", "daemon off;"]
