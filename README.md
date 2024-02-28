# nginx-proxy-reverse-kubernetes

**Gerar as imagens docker localmente**

- API1 (/posts)

  `cd api1`

  `docker build . -t api1:local`

- API2 (/comments)

  `cd api2`

  `docker build . -t api2:local`

- NGINX

  `cd nginx`

  `docker build . -t nginx:local`


**Aplicar os arquivos do Kubernetes**

`kubectl apply -f namespace.yaml`

`kubectl apply -f nginx-deployment.yaml`

`kubectl apply -f api1-deployment.yaml`

`kubectl apply -f api2-deployment.yaml`

`kubectl apply -f api1-service.yaml`

`kubectl apply -f api2-service.yaml`


**Endpoints**

`curl --request GET|POST|PUT|PATCH --url http://localhost/posts`

`curl --request GET|POST|PUT|PATCH --url http://localhost/comments`
