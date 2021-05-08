# Web API design

## What does REST stand for?

Representational State Transfer

## REST APIs are designed around a ____.

REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.

## What is an identifer of a resource? Give an example.

 identifier is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be:

 'https://adventure-works.com/orders/1'

## What are the most common HTTP verbs?

GET, POST, PUT, PATCH, and DELETE.

## What should the URIs be based on?

URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

## Give an example of a good URI.

'https://adventure-works.com/orders'

## What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?

 Chatty APIs expose a large number of small resources. Such an API may require a client application to send multiple requests to find all of the data that it requires. and it's a bad thing.

 ## What status code does a successful GET request return? What status code does an unsuccessful GET request return?

A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

## What status code does a successful POST request return?

If a POST method creates a new resource, it returns HTTP status code 201 (Created).

## What status code does a successful DELETE request return?

If the delete operation is successful, the web server should respond with HTTP status code 204.