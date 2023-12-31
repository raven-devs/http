# Status Code

## 2xx: Successful

### 200 OK

The request is OK.

### 201 Created

The request is complete, and a new resource is created.

### 204 No Content

A status code and a header are given in the response, but there is no entity-body in the reply.

## 4xx: Client Error

### 400 Bad Request

The server did not understand the request.

### 401 Unauthorized

The requested resource needs a username and a password.

### 403 Forbidden

Access is forbidden to the requested resource.

### 404 Not Found

The server can not find the requested resource.

### 405 Method Not Allowed

The method specified in the request is not allowed.

### 406 Not Acceptable

The server can only generate a response that is not accepted by the client.

### 408 Request Timeout

The request took longer than the server was prepared to wait.

### 409 Conflict

The request could not be completed because of a conflict.

### 410 Gone

The requested resource is no longer available.

### 412 Precondition Failed

The pre condition given in the request evaluated to false by the server.

### 413 Request Entity Too Large

The server will not accept the request, because the request entity is too large.

### 414 Request-url Too Long

The server will not accept the request, because the url is too long. Occurs when you convert a "post" request to a "get" request with a long query information.

### 415 Unsupported Media Type

The server will not accept the request, because the mediatype is not supported.

## 5xx: Server Error

### 500 Internal Server Error

The request was not completed. The server met an unexpected condition.

### 501 Not Implemented

The request was not completed. The server did not support the functionality required.

### 502 Bad Gateway

The request was not completed. The server received an invalid response from the upstream server.

### 503 Service Unavailable

The request was not completed. The server is temporarily overloading or down.

### 504 Gateway Timeout

The gateway has timed out.
