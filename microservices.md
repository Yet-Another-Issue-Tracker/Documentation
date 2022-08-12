# Microservices
the scope of this document is to define the number of microservices and the domain they should cover, that is the APIs they should implement

## issue-service
The issue service is responsible for the management of Projects, Sprints and Issues.
A Project can have N Sprints and a Sprint can have M Issues.

The service is written in go, and to develop it the following documentation has been browsed and used as reference:
* error handling: https://earthly.dev/blog/golang-errors/
* middleware: https://www.nicolasmerouze.com/middlewares-golang-best-practices-examples
* project layout: https://github.com/golang-standards/project-layout + https://www.dudley.codes/posts/2020.05.19-golang-structure-web-servers/

## notification-service
The idea is to write the service using [quarkus](https://quarkus.io/). 
The service will consume messages on from a queue (probably a kafka topic) in order to send email using Twilio API. 
It will also expose an API to send email synchronously.

## user-service
The service is responsible for user creation, login/logout using Auth0 API. 
It will also manage resource bindings, used to assign permissions to a user for a specific resource (ex: project permissions) 

## file-service
The service manages file upload and download.
It will leverage different drivers (DB, S3, Google Storage)