# demo-springboot-api-h2
Springboot + API + JPA (H2) + Dockerized

## Package the jar
```
cd <project root>
mvn package
```

## Deploy on Docker
Build the Image
```
docker build -t springboot/demo-api-h2 .
```

Create container (Run it on 8082 port on host)
```
docker run -p 8082:8080 springboot/demo-api-h2
```

## Test APIs
GET http://localhost:8082/api/v1/users

GET http://localhost:8082/api/v1/users/<user id>

POST http://localhost:8082/api/v1/users

Sample request body:
```
{
	"firstName": "John",
	"lastName": "Doe",
	"email": "xyz@xyz.com"
}
```