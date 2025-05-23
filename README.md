# Spring Cloud Gateway
Proxy inverso que enruta las peticiones a los distintos servicios :

http://localhost:8080/demo1/saludo

http://localhost:8080/demo2/saludo

## Desplegar con Docker Compose:
docker-compose -f docker-compose-spring-cloud-gateway.yml down -v
docker-compose -f docker-compose-spring-cloud-gateway.yml build --no-cache
docker-compose -f docker-compose-spring-cloud-gateway.yml up -d