FROM almalinux:9

# Update packages and install Nginx + unzip
RUN dnf update -y && \
    dnf install -y nginx unzip && \
    dnf clean all

# Remove default Nginx HTML content
RUN rm -rf /usr/share/nginx/html/*

# Copy frontend ZIP from local machine into the image
COPY frontend-v3.zip /tmp/frontend-v3.zip

# Extract frontend files and remove ZIP
RUN unzip /tmp/frontend-v3.zip -d /usr/share/nginx/html/ && \
    rm -f /tmp/frontend-v3.zip

# Nginx listens on port 80
EXPOSE 80

# Start Nginx in foreground
CMD ["nginx", "-g", "daemon off;"]