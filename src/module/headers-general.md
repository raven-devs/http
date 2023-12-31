# Headers: General

These header fields have general applicability for both request and response messages.

## Cache-control

The Cache-Control general-header field is used to specify directives that MUST be obeyed by all caching system.

```text
Cache-control: no-cache
```

## Connection

The Connection general-header field allows the sender to specify options that are desired for that particular connection and must not be communicated by proxies over further connections.

```text
Connection: keep-alive
```

## Date

All HTTP date/time stamps MUST be represented in Greenwich Mean Time (GMT), without exception.

```text
Date: Sun Nov  6 08:49:37 1994
```

## Pragma

The Pragma general-header field is used to include implementation- specific directives that might apply to any recipient along the request/response chain. The only directive defined in HTTP/1.0 is the no-cache directive and is maintained in HTTP 1.1 for backward compatibility. No new Pragma directives will be defined in the future.

```text
Pragma: no-cache
```

## Trailer

The Trailer general field value indicates that the given set of header fields is present in the trailer of a message encoded with chunked transfer-coding.

```text
Trailer : field-name
```

## Transfer-Encoding

The Transfer-Encoding general-header field indicates what type of transformation has been applied to the message body in order to safely transfer it between the sender and the recipient. This is not the same as content-encoding because transfer-encodings are a property of the message, not of the entity-body.

```text
Transfer-Encoding: chunked
```

## Upgrade

The Upgrade general-header allows the client to specify what additional communication protocols it supports and would like to use if the server finds it appropriate to switch protocols.

```text
Upgrade: HTTP/2.0, SHTTP/1.3, IRC/6.9, RTA/x11
```

## Via

The Via general-header must be used by gateways and proxies to indicate the intermediate protocols and recipients. For example, a request message could be sent from an HTTP/1.0 user agent to an internal proxy code-named "fred", which uses HTTP/1.1 to forward the request to a public proxy at nowhere.com, which completes the request by forwarding it to the origin server at www.ics.uci.edu. The request received by www.ics.uci.edu would then have the following Via header field:

```text
Via: 1.0 fred, 1.1 nowhere.com (Apache/1.1)
```

## Warning

The Warning general-header is used to carry additional information about the status or transformation of a message which might not be reflected in the message.

```text
Warning : warn-code SP warn-agent SP warn-text SP warn-date
```
