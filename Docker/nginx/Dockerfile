FROM almalinux:9
RUN  dnf update -y && /
     dnf install nginx -y 
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]