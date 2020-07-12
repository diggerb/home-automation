# Home Automation Project

The documentation how the project can be found in the Documentation.md file in the repository's root directory

## Project Context

### Mantra

This is my first attempt at a REST API (Representational State Transfer). 

### Project Aims

To allow many devices (most likely Raspberry Pis) to connect to my network(s) and comunicate seamlessly via a set of microservices bound together by a RESTful API. 

## What is a RESTful API?

A RESTful API simply means that the API follow a set of 6 principles. One of the properties is that the API must be stateless and does not store any context. It therefore must not remember what has previously been asked or by whom. Hence every request must contain all of the information required to process the request as the information cannot be found elsewhere.

The other properties can be found [here.](https://restfulapi.net/rest-architectural-constraints/) (external link)

These requests will be made over http/https and hence I shall be following the accompanying standards.

## The Plan

First, I will be developing the Device Registry Service. This stores information on all of the devices on the network that can be controlled and hence it only needs the simply ability to create read and delete resources.

Resources are simply objects that the API stores and can refer to anything (for exmaple, a device). Multiple resources of the same type are known as a collection. 

Then I will develop further functionality on top of this API such as WOL functionality and maybe port over and extend my Tram-Times app.

## Methods

Below are the methods I shall be implementing in to my project. There are other methods however they shall be implemented at a later date as required.

### `GET` Requests

This will solely be used for retrieving information and should never modify anything. As such, repeating a `GET` request should always retrieve exactly the same information. This type of request is known an *idempotent* request.

### `POST` Requests

`POST` requests are used to create new resources. They are not idempotent as is it not safe to repeat a `POST` requesto many times. This would create as many new resources as requests have been made.

### `DELETE` Requests

This is Ronseal (it does exactly what it says on the tin). This is defined to be idempotent as repeating a `DELETE` request has the same effect as making the request once. Hence it is also safe to repeat multiple times. 

