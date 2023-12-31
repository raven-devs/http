# Headers: Client request

These header fields are applicability only for request messages.

## Accept

The Accept request-header field can be used to specify certain media types which are acceptable for the response.

```text
Accept: text/plain
```

## Accept-Charset

The Accept-Charset request-header field can be used to indicate what character sets are acceptable for the response.

```text
Accept-Charset: utf-8
```

The Accept-Charset header is a crucial part of HTTP that facilitates content negotiation, ensuring that content is delivered in a character encoding that is best suited to the client's capabilities.

## Accept-Encoding

The Accept-Encoding request-header field is similar to Accept, but restricts the content-codings that are acceptable in the response.

```text
Accept-Encoding: compress, gzip
```

The Accept-Encoding header is a fundamental part of HTTP, enabling efficient content transfer and optimization of web resources. By supporting and correctly handling various content encodings, both clients and servers contribute to more efficient and faster web communication.

## Accept-Language

The Accept-Language request-header field is similar to Accept, but restricts the set of natural languages that are preferred as a response to the request.

```text
Accept-Language: fr-FR
```

The Accept-Language header is a key element in making the web more inclusive and user-friendly, enabling content to be delivered in the language that best suits each user's preference and needs. The server might also include a `Content-Language` header in the response indicating the language of the returned content (e.g., `Content-Language: fr-FR`). If the requested language version of the content is not available, the server might fall back to a default language, often English, or choose the next preferred language specified by the client.

## Authorization

The Authorization header in HTTP is used to transmit credentials from a client to a server, typically for the purpose of authenticating the client. This header is a fundamental part of HTTP security, allowing users or applications to securely access protected resources.

```text
Authorization: BASIC Z3Vlc3Q6Z3Vlc3QxMjM=
```

- Basic Authentication: The header might include a username and password encoded in Base64. The format would look like this: Authorization: Basic [encoded-credentials].

- Bearer Token: In token-based authentication, such as with OAuth 2.0, the header carries a token. It would be formatted like this: Authorization: Bearer [token].

## Cookie

The Cookie request-header field value contains a name/value pair of information stored for that URL.

```text
Cookie: name1=value1;name2=value2;name3=value3
```

## Expect

The Expect request-header field is used to indicate that particular server behaviors are required by the client.

```text
Expect : 100-continue | expectation-extension
```

If a server receives a request containing an Expect field that includes an expectation-extension that it does not support, it must respond with a 417 (Expectation Failed) status.

## Host

The Host request-header field is used to specify the Internet host and port number of the resource being requested. A host without any trailing port information implies the default port, which is 80.

```text
Host: www.w3.org
```

## If-Match

The If-Match request-header field is used with a method to make it conditional. This header request the server to perform the requested method only if given value in this tag matches the given entity tags represented by ETag. An asterisk (*) matches any entity, and the transaction continues only if the entity exists. If none of the entity tags match, or if "*" is given and no current entity exists, the server must not perform the requested method, and must return a 412 (Precondition Failed) response.

```text
If-Match: "xyzzy"
If-Match: *
```

## If-None-Match

The If-None-Match request-header field is used with a method to make it conditional. This header request the server to perform the requested method only if none of the given value in this tag matches the given entity tags represented by ETag. An asterisk (*) matches any entity, and the transaction continues only if the entity does not exist.

```text
If-None-Match: "xyzzy"
If-None-Match: *
```

## If-Modified-Since

The If-Modified-Since request-header field is used with a method to make it conditional. If the requested URL has not been modified since the time specified in this field, an entity will not be returned from the server; instead, a 304 (not modified) response will be returned without any message-body. If none of the entity tags match, or if "*" is given and no current entity exists, the server must not perform the requested method, and must return a 412 (Precondition Failed) response.

```text
If-Modified-Since: Sat, 29 Oct 1994 19:43:31 GMT
```

## If-Unmodified-Since

The If-Unmodified-Since request-header field is used with a method to make it conditional. If the requested resource has not been modified since the time specified in this field, the server should perform the requested operation as if the If-Unmodified-Since header were not present. If the request normally would result in anything other than a 2xx or 412 status, the If-Unmodified-Since header should be ignored.

```text
If-Unmodified-Since: Sat, 29 Oct 1994 19:43:31 GMT
```

## If-Range

The If-Range request-header field can be used with a conditional GET to request only the portion of the entity that is missing.

```text
If-Range: Sat, 29 Oct 1994 19:43:31 GMT
```

Here if the document has not been modified since the given date, the server returns the byte range (a portion) given by the Range header otherwise, it returns all of the entity content.

## Max-Forwards

The Max-Forwards request-header field provides a mechanism with the TRACE and OPTIONS methods to limit the number of proxies or gateways that can forward the request to the next inbound server. The Max-Forwards header field may be ignored for all other methods defined in HTTP specification.

```text
Max-Forwards : 5
```

## Proxy-Authorization

The Proxy-Authorization request-header field allows the client to identify itself (or its user) to a proxy which requires authentication. The Proxy-Authorization field value consists of credentials containing the authentication information of the user agent for the proxy and/or realm of the resource being requested.

```text
Proxy-Authorization: BASIC Z3Vlc3Q6Z3Vlc3QxMjM=
```

## Range

The Range request-header field specifies the partial range(s) of the content requested from the document.

The first 500 bytes:

```text
Range: bytes=0-499
```

The second 500 bytes:

```text
Range: bytes=500-999
```

## From

The From request-header field contains an Internet e-mail address for the human user who controls the requesting user agent. This header field may be used for logging purposes and as a means for identifying the source of invalid or unwanted requests.

```text
From: webmaster@w3.org
```

## Referer

The Referer request-header field allows the client to specify the address (URI) of the resource from which the URL has been requested.

```text
Referer: http://www.tutorialspoint.org/http/index.htm
```

## User-Agent

The User-Agent request-header field contains information about the user agent originating the request.

```text
User-Agent: Mozilla/4.0 (compatible; MSIE5.01; Windows NT)
```

## TE

The TE request-header field indicates what extension transfer-coding it is willing to accept in the response and whether or not it is willing to accept trailer fields in a chunked transfer-coding.

```text
TE: deflate
```
