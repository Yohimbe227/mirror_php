FROM nginx:latest

# Add the Debian backports and main repositories
RUN apt-get update && apt-get install -y \
    software-properties-common \
    && add-apt-repository 'deb http://deb.debian.org/debian bookworm main contrib non-free' \
    && add-apt-repository 'deb http://deb.debian.org/debian bookworm-updates main contrib non-free' \
    && add-apt-repository 'deb http://deb.debian.org/debian-security bookworm-security main contrib non-free' \
    && apt-get update

# Install nginx-full and required modules
RUN apt-get update && apt-get install -y nginx-full \
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

# Expose ports
EXPOSE 80 443

# Start nginx
CMD ["nginx", "-g", "daemon off;"]

