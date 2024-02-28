FROM node:lts-alpine
LABEL Author="Welber Macedo" 
RUN mkdir /app
WORKDIR /app
COPY . /app
RUN npm i json-server@0.9.2;
COPY ./api.json /app/api.json
RUN cd /app; chmod 777 api.json;
EXPOSE 3000
CMD ["npx", "json-server", "--host", "0.0.0.0", "/app/api.json", "--no-cors"]