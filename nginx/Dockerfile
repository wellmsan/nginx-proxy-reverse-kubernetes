FROM nginx:latest
LABEL Author="Welber Macedo" 
COPY ./nginx.conf /etc/nginx/nginx.conf
EXPOSE 80
ENTRYPOINT [ "nginx" ]
CMD [ "-g", "daemon off;" ]