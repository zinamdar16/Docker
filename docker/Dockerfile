
# 1. Base Image

FROM nginx:latest


# 2. Labels

LABEL maintainer="yourname@example.com"
LABEL version="1.0"
LABEL description="Custom NGINX Docker image"


# 3. Set Environment Variables

ENV NGINX_PORT=80 \
    NGINX_ROOT=/usr/share/nginx/html


# 4. Create directories and set permissions

RUN mkdir -p $NGINX_ROOT && \
    chown -R nginx:nginx $NGINX_ROOT


# 5. Copy files

COPY . .

# Optional: custom nginx config
# COPY nginx.conf /etc/nginx/nginx.conf


# 6. Set working directory

WORKDIR $NGINX_ROOT


# 7. Expose Port

EXPOSE $NGINX_PORT


# 8. Define Entry Point and CMD


# Entrypoint for setting up environment or configuration
#ENTRYPOINT ["/docker-entrypoint.sh"]

# CMD is passed as argument to ENTRYPOINT
CMD ["nginx", "-g", "daemon off;"]

