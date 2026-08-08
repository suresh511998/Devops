FROM almalinux:9
RUN  dnf update -y && \
     dnf install nginx -y 
# Remove default Nginx HTML
RUN rm -rf /usr/share/nginx/html/*
COPY frontend-v3.zip /tmp/frontend-v3.zip 
RUN unzip /tmp/frontend-v3.zip -d /usr/share/nginx/html/ && \
    rm -rf /tmp/frontend-v3.zip 
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]