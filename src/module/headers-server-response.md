# Headers: Server response

These header fields are applicability only for response messages.

## Accept-Ranges

The Accept-Ranges response-header field allows the server to indicate its acceptance of range requests for a resource.

```text
Accept-Ranges: bytes
```

## Age

The Age response-header field conveys the sender's estimate of the amount of time since the response (or its revalidation) was generated at the origin server. Age values are non-negative decimal integers, representing time in seconds.

```text
Age: 1030
```

## ETag

The ETag response-header field provides the current value of the entity tag for the requested variant.

```text
ETag: "xyzzy"
```

## Location

The Location response-header field is used to redirect the recipient to a location other than the Request-URI for completion.

```text
Location: http://www.tutorialspoint.org/http/index.htm
```

## Proxy-Authenticate

The Proxy-Authenticate response-header field must be included as part of a 407 (Proxy Authentication Required) response.

## Retry-After

The Retry-After response-header field can be used with a 503 (Service Unavailable) response to indicate how long the service is expected to be unavailable to the requesting client.

```text
Retry-After: Fri, 31 Dec 1999 23:59:59 GMT
Retry-After: 120
```

## Server

The Server response-header field contains information about the software used by the origin server to handle the request.

```text
Server: Apache/2.2.14 (Win32)
```

## Set-Cookie

The Set-Cookie response-header field contains a name/value pair of information to retain for this URL.

```text
Set-Cookie: NAME=VALUE; OPTIONS
```

## Vary

The Vary response-header field specifies that the entity has multiple sources and may therefore vary according to specified list of request header(s).

```text
Vary: Accept-Language, Accept-Encoding
```

## WWW-Authenticate

The WWW-Authenticate response-header field must be included in 401 (Unauthorized) response messages. The field value consists of at least one challenge that indicates the authentication scheme(s) and parameters applicable to the Request-URI.

```text
WWW-Authenticate: BASIC realm="Admin"
```
