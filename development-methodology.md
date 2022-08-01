# How to design the system
This document provides the guideline that I followed to develop the Issue Tracker system. 
This is the mental track that I thought was the best way to approach the problem and design a solution.
I followed a top-down approach, starting from the high level of the architecture and customer journey through the bottom of DB schema, i believe that it is easier to understand what the system should do from a user perspective and then define the technical details of the implementation. 

## Define the Features
First of all we need to know what the system should do, both from an end user perspective and from a technical point of view (authentication, infrastructure etc). 

Checkout the document `project-specification.md` to view the full list of features and the phase of the project

## Define the Architecture
Once the features and constraints are defined we should begin to think about the architecture. [Here](https://docs.google.com/presentation/d/1k3RajdNzf6ttPJXNC8LM1m64zh2PVCmN1LBDGD2KURc/edit#slide=id.p) or in the file `architecture.png` you can find the components architecture, it is now a low level detailed architecture but it focuses more on listing the components and the interactions between them.

## Define the Customer Journey and the UI
We know the features but we don't know how they are being consumed by the end user and so we are not able to define the API interface of the services. 
Defining the customer journey and the UI of the website we will be able to also clarify the interface of the api and write some Open API Specification. 
[Here](https://www.figma.com/file/yapnLLAbBXQKZGPpbZ7DGN/yait---customer-journey?node-id=0%3A1) or in the file `customer-journey.pdf` you can find the customer journey. 

## Define the microservices 
Once the customer journey is defined the domain of the services should be clearer, we can then define the number of services and the domain they should cover. 
For this projects 4 differents microservices has been defined, the specification can be found in this file `microservices.md`

### Define the API interface of each service
The substep of defining microservices is to write the Open API Specification for each API of the service. This step is mandatory for the development of both Front End and Back End services. API first is in my opinion the safer way to develop a system in order to parallelize the development of FE and BE. In my case I will do both the parts and so I can not work in parallel. 

## Define the DB schema
Finally if the API interface are well defined also should be the entity of our system, so is now time to define the Database schema, that is the ER schema, checkout the `er-schema.png` file. 


