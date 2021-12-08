# Spring Data REST
Spring Data REST + REST Repositories + Spring Data JPA + H2 database + Lombok

Spring Data REST is part of Spring Data project and makes it easy to build REST web services. 

Spring Data REST analyzes your application’s domain model and expose it as REST endpoint.


## Run
mvn clean spring-boot:run

## For rest calls, 
install the chrome plugin: ADVANCED REST CLIENT (ARC). 
Download link: https://chrome.google.com/webstore/detail/advanced-rest-client/hgmloofddffdnphfgcellkdfbfbjeloo 
ARC is similar to Postman
Open ARC from google -> top left click on 'APP' In ARC enter:

## Get all Users:
HTTP Method: GET
Request url: http://localhost:8080/api/users


## Get user By ID
HTTP Method: GET
Request url: http://localhost:8080/api/users/1


## Create a new user
Method: POST
Body content type: application/json
Request url: http://localhost:8080/api/users
insert in the  nel body:
{
  "firstName": "Enrico",
   "lastName": "Milano",
   "email": "milano@gmail.com"
}


## Verify User create before, By ID
HTTP Method: GET
Request url: http://localhost:8080/api/users/6

Please note: with http://localhost:8080/api/users/6  you don't see the new user because the pagination is set to 4 in application.properties
To see it : http://localhost:8080/api/users?page=1 (second page)



## Modifiy User
HTTP Method: PUT
insert in the  nel body:
{
  "firstName": "Enrico",
   "lastName": "Roma",
   "email": "roma@gmail.com"
}


## Verify User update before, By ID
HTTP Method: GET
Request url: http://localhost:8080/api/users/6



## Delete User
HTTP Method: DELETE
Request url: http://localhost:8080/api/users/6


## Customize default Pagination
Default Pagination is in application.properties file
HTTP Method: GET
Request url: http://localhost:8080/api/users?page=0&size=3


## Sorting
HTTP Method: GET
Request url: http://localhost:8080/api/users?sort=fisrtName
