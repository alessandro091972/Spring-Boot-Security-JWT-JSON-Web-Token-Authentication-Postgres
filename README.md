# Spring-Boot-Security-JWT-JSON-Web-Token-Authentication-Postgres
Spring Boot Security + JWT (JSON Web Token) Authentication using POSTGRES example

Create the database on postgres: test
The 'user' table will then be generated at runtime

# Run
mvn clean spring-boot:run

# REST Call
For rest calls, install the chrome plugin: ADVANCED REST CLIENT (ARC).
Download link: https://chrome.google.com/webstore/detail/advanced-rest-client/
ARC is similar to Postman

Open ARC from google -> top left click on 'APP'
In ARC enter:

# Enter your database credentials
Request URL: http://localhost:8080/register
Method: POST
Body content type: application/json

inserire nel body:
{
  "username": "yourUsername",
  "password": "yourPassword"
}


# Authentication
Request URL: http://localhost:8080/authenticate
Method: POST
Body content type: application/json

inserire nel body:
{
  "username": "yourUsername",
  "password": "yourPassword"
}


# To see the protected page
Request URL: http://localhost:8080/hello
Method: GET
--> Add HEADER 
Header name =  authorization
Header value=  Bearer TOKEN (preso da http://localhost:8080/authenticate)    
