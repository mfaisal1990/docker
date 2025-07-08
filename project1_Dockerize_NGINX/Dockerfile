#Base Image
FROM nginx:alpine

LABEL Maintainer="Muhammad Faisal muhammadfaisal1990@gmail.com"

#Copy index.html to /usr/share/nginx/html
COPY index.html /usr/share/nginx/html

#Expose NGINX port
EXPOSE 80

#Start NGINX service
CMD ["nginx", "-g", "daemon off;"]
