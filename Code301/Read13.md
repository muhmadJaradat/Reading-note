# CRUD

## Which HTTP Status Code to Use for Every CRUD App

The HTTP specification defines many status codes we can use when responding to our clients. Some APIs only use the most basic codes and define their own error signaling mechanisms on top of it; others want to make full use of HTTPs collection of codes to tell their clients what’s going on. If you belong to the latter, this article is for you. This guide walks through the various CRUD operations and which status codes you should be using for clean API design.

## HTTP Status CodesPermalink

A status code is a number higher than 100 and smaller than 600 that is part of a HTTP response. The first digit defines the class of the status. A status code comes with a reason phrase. The code is for programmatic recognition the phrase is for humans to understand what happened.

## Status Codes Based On REST Methods

* 100’s = the request has been received from the client and waiting for the server to comply.

* 200’s = success request, tells the client that the request has been accepted.

* 300’s = redirection, which means that the request that has been sent to the server is invalid.

* 400’s = client error, invalid request.

* 500’s = server errors

### What is a status code 202?

202 Accepted - Often used for asynchronous processing. This code tells the client that the request was valid, but its processing will finish sometime in the future. 

### What is a status code 308? 

308 Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore.

### What code would you use if an update didn’t return data to a client?

204 No Content

### What is the ‘Forbidden’ status code?

The client has authorized or doesn’t need to authorize itself, but still has no permissions to access the resource.

### Why do we need to pull our MongoDB database string out of our server and put it into our .env?

To keep it secure

### what is middleware?

Middleware is software that provides common services and capabilities to applications outside of what’s offered by the operating system. Data management, application services, messaging, authentication, and API management are all commonly handled by middleware.

### what does app.use(express.json()) do?

express. json() is a method inbuilt in express to recognize the incoming Request Object as a JSON Object. This method is called as a middleware in your application using the code: app. … urlencoded() is a method inbuilt in express to recognize the incoming Request Object as strings or arrays

### what does the /:id mean in a route?

The Route ID is a number which uniquely identifies the route. The name or title of a route is NOT unique. So if you want to refer to a specific route to mention a problem in an email, you better provide the Route ID.

### what is the difference beween PUT and PATCH?

The main difference between the PUT and PATCH method is that the PUT method uses the request URI to supply a modified version of the requested resource which replaces the original version of the resource, whereas the PATCH method supplies a set of instructions to modify the resource

### what does a 500 error status code mean?

The HyperText Transfer Protocol (HTTP) 500 Internal Server Error server error response code indicates that the server encountered an unexpected condition that prevented it from fulfilling the request. This error response is a generic “catch-all” response.