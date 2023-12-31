# Headers: Entity

These header fields define metainformation about the entity-body.

## Allow

The Allow entity-header field lists the set of methods supported by the resource identified by the Request-URI. 

```text
Allow: GET, HEAD, PUT
```

## Content-Encoding

The content-coding is a characteristic of the entity identified by the Request-URI. If the content-encoding of an entity in a request message is not acceptable to the origin server, the server should respond with a status code of 415 (Unsupported Media Type).

```text
Content-Encoding: gzip
```

## Content-Language

The Content-Language entity-header field describes the natural language(s) of the intended audience for the enclosed entity. The primary purpose of Content-Language is to allow a user to identify and differentiate entities according to the user's own preferred language.

```text
Content-Language: en
```

## Content-Length

The Content-Length entity-header field indicates the size of the entity-body, in decimal number of OCTETs, sent to the recipient or, in the case of the HEAD method, the size of the entity-body that would have been sent had the request been a GET.

```text
Content-Length: 3495
```

## Content-Location

The Content-Location entity-header field may be used to supply the resource location for the entity enclosed in the message when that entity is accessible from a location separate from the requested resource's URI.

```text
Content-Location: http://www.tutorialspoint.org/http/index.htm
```

## Content-Range

The Content-Range entity-header field is sent with a partial entity-body to specify where in the full entity-body the partial body should be applied.

The first 500 bytes:

```text
Content-Range : bytes 0-499/1234
```

The second 500 bytes:

```text
Content-Range : bytes 0-499/1234
```

## Content-Type

The Content-Type entity-header field indicates the media type of the entity-body sent to the recipient or, in the case of the HEAD method, the media type that would have been sent had the request been a GET.

```text
Content-Type: text/html; charset=ISO-8859-4
```

## Expires

The Expires entity-header field gives the date/time after which the response is considered stale.

```text
Expires: Thu, 01 Dec 1994 16:00:00 GMT
```

## Last-Modified

The Last-Modified entity-header field indicates the date and time at which the origin server believes the variant was last modified.

```text
Last-Modified: Tue, 15 Nov 1994 12:45:26 GMT
```
