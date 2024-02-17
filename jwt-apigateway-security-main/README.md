# jwt-apigateway-security
- Microservices : 
  - identity-service : Security
  - restaurant-service : Bussiness Logic
  - swiggy-app : Bussiness Logic
  - swiggy-gateway : Centralize request
  - swiggy-service-registry : Load balancer, Discovery, Register Microservices

- Database
  - docker-compose up

## Register an user con ApiGateway
- POST 'http://localhost:8080/auth/register'
```
{
    "name":"Basant",
    "password":"Pwd1",
    "email":"basant@gmail.com"
}
```

## Generate token con ApiGateway
- POST 'http://localhost:8080/auth/token'
```
{
    "username":"Basant",
    "password":"Pwd1"
}
```

## Access Swiggy-app
- GET 'http://localhost:8080/swiggy/37jbd832'
- 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJCYXNhbnQiLCJpYXQiOjE2NzkwNTU4MDIsImV4cCI6MTY3OTA1NzYwMn0.Q0bwS5_16q1Z8K-p_flpmyRoJNFCyOhU2AMKSNYh66o'



## Access Restaurant-service
- GET 'http://localhost:8080/restaurant/orders/status/37jbd832'
- 'Authorization: Bearer eyJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJCYXNhbnQiLCJpYXQiOjE2NzkwNTU1MDcsImV4cCI6MTY3OTA1NzMwN30.9nNAW1rx8RoTIrhn5Abtzg7RplvT9_d-U5EOwUcJZq8'


