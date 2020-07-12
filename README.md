# Home Automation Project

## Project Context

### Mantra

This is my first attempt at a REST API (Representational State Transfer). 

### Aims

The allow many devices (most likely Raspberry Pis) to connect to my network(s) and comunicate seamlessly. 

## What is a RESTful API?

RESTful means the code will be stateless and will not store any content. It therefore must not remember what has previously been asked. Hence every request must contain all of the information required to process the request, as the information cannot be found elsewhere.

These requests will be made over http/https and hence I shall be following the accompanying standards.

### GET Requests

This will solely be used for retrieving information and should never modify anything. As suchs repeating a `GET` request should always retrieve exactly the same information. This type of request is known as being *idempotent*.

### POST Requests

`POST` requests are used to create new resources.

