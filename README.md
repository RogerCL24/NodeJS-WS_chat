# Chat background

## API REST
An API is a set of subroutines, processes, functions, or methods that a software <sub>1</sub> offers so that other software <sub>2</sub> can interact with it. It doesn't necessarily have to be other software <sub>2</sub>, the same software <sub>1</sub> can expose an API so that it can interact with itself. API stands for Application Programming Interface and basically allow us to interact with software. 

For instance, we use API's in Python or Java so as to use functions already implemented.

### REST-like API
They are the ones that allow us to create web applications or mobile applications that connect to a server via client-server. So understanding that API is a set of functions, methods or subroutines that a software exposes to be able to interact with it, in this case it is the same because we are going to expose some functions that will allow a client, either in a browser or an application mobile, that connect with our backend application via API-REST.

<p align="center">

<img src="https://github.com/RogerCL24/NodeJS-WS_chat/assets/90930371/4ff32ad6-b496-4474-aef5-6dc73fe21e8e"/>
</p>

### HTTP
REST is based on the HTTP protocol to be able to expose its architecture, even any web browser to any web page uses the REST architecture under the HTTP protocol. 

The HTTP protocol allows us to expose a series of rules.

A protocol is a series of steps that you must follow to achieve a goal. It is not an algorithm, algorithms are a series of steps to solve a problem, but a protocol is a series of steps that you must perform to achieve a specific objective.

The protocol allows us to expose a standard so that we all speak the same language and follow the same rules, otherwise everyone would make their own rules and it would no longer be a standard.

The HTTP protocol is the one on which the REST architecture is based to expose our APIs. It is based on a client-server communication where the client makes a request and the server gives a response. 

Example:

**HTTP REQUEST**
```http
GET /index.html HTTP/1.1
Host: www.example.com
Referer: www.google.com
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:45.0) Gecko/20100101 Firefox/45.0
Connection: keep-alive
```
- **HTTP method**: GET.
- **Path**: /index.html, the path lead us to where we want to request.
- **HTTP protocol version**: 1.1.
- **Headers**: _Host_, _Referer_, _User-Agent_ and _Connection_.

**HTTP RESPONSE**
```html
HTTP/1.1 200 OK
Date: Fri, 31 Dec 2003 23:59:59 GMT
Content-Type: text/html
Content-Length: 1221

<html lang="eo">
<head>
<meta charset="utf-8">
<title>Site title</title>
</head>
<body>
<h1>Host principal Page</h1>
(Content)
.
.
.
</body>
</html>
```
- **HTTP protocol version**: 1.1.
- **Response code**: 200
- **Response code text**: OK
- **Headers**: _Date_, _Content-Type_ and _Content-Length_
- **Body response**: The server response, which we are going to process to show it to the client from a browser or a mobile app.

**HTTP METHODS**

They identify the request type the client is executing to the server, we will only comment the standards methods:
- **GET**: It helps us to make a request for the server to send information to the client. 
- **POST**: It is used to send information from the client to the server. This way we create new resources (new users, new community comments, answers to a question box, give a like...)
- **PUT**: To update an entire resource. If the resource exists and we want to update it, we will use the **PUT** method changing the properties we want to convert.
- **DELETE**: To delete a resource.
- **PATCH**: To partially update a resource, it is useful to only update a part of the resource and not all of it.
- **HEADER**: It allows us to query the existence of a resource, it is different from the GET method because it asks the server to send it the resource, while HEADER only asks the server if it exists, it does not send any resource.
- **OPTIONS**: It is used natively by browsers. It will allow the browser to validate a request that any method/verb be used, this is done to verify that domain A.com can make these requests to domain B.com. This is done to prevent anyone from making requests from other domains.

Actually this is definded as a concept, **CORS**, which dictates if you want allow or not the requests from the domain A.com to the domain B.com, this is defined when you create your API, for example you can allow only resquests from your subdomains to the domain and any other requests from other web pages will be restricted to avoid CORS attacks.
>[!NOTE]
> If you are doing a backend client pointing to an API, this backend client do not execute the **OPTION** requests, owing to the fact that they do not have domain, furthermore they execute request straightforward to the server, unlike the browsers.

## NODE.JS 

