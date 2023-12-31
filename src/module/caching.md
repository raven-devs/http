# Caching

HTTP is typically used for distributed information systems, where performance can be improved by the use of response caches. The HTTP/1.1 protocol includes a number of elements intended to make caching work.

The goal of caching in HTTP/1.1 is to eliminate the need to send requests in many cases, and to eliminate the need to send full responses in many other cases.

The basic cache mechanisms in HTTP/1.1 are implicit directives to caches where server-specifies expiration times and validators. We use the Cache-Control header for this purpose.

The Cache-Control header allows a client or server to transmit a variety of directives in either requests or responses. These directives typically override the default caching algorithms. The caching directives are specified in a comma-separated list.

```text
Cache-control: no-cache
```

## Cache Request Directive and Description

### no-cache

A cache must not use the response to satisfy a subsequent request without successful revalidation with the origin server. That means a client will cache the response, but the client will check the server before using that cached data: "data has changed on the server or not?" with help of If-Modified-Since, If-None-Match and ETag headers.

### no-store

The cache should not store anything about the client request or server response. That means a client will not make any caching operation.

### max-age = seconds

Indicates that the client is willing to accept a response whose age is no greater than the specified time in seconds.

### max-stale [ = seconds ]

Indicates that the client is willing to accept a response that has exceeded its expiration time. If seconds are given, it must not be expired by more than that time.

### min-fresh = seconds

Indicates that the client is willing to accept a response whose freshness lifetime is no less than its current age plus the specified time in seconds.

### no-transform

Do not convert the entity-body.

### only-if-cached

Do not retrieve new data. The cache can send a document only if it is in the cache, and should not contact the origin-server to see if a newer copy exists.

## Cache Response Directive and Description

### public

Indicates that the response may be cached by any cache.

### private

Indicates that all or part of the response message is intended for a single user and must not be cached by a shared cache.

### no-cache

A cache must not use the response to satisfy a subsequent request without successful revalidation with the origin server.

### no-store

The cache should not store anything about the client request or server response.

### no-transform

Do not convert the entity-body.

### must-revalidate

The cache must verify the status of stale documents before using it and expired one should not be used.

### proxy-revalidate

The proxy-revalidate directive has the same meaning as the must- revalidate directive, except that it does not apply to non-shared user agent caches.

### max-age = seconds

Indicates that the client is willing to accept a response whose age is no greater than the specified time in seconds.

### s-maxage = seconds

The maximum age specified by this directive overrides the maximum age specified by either the max-age directive or the Expires header. The s-maxage directive is always ignored by a private cache.
