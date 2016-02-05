# HTTP/2 The (not so) new Language of the Web
> by: [Adrian Cardenas][1]  
> source: [High Performance Browser Networking][2]

## Preface

### History of HTTP 1.x

* Proposed by Tim Berners-Lee & team in 1989
* HTTP 0.9 first documented in 1991
* HTTP 1.0 oficially documented in 1996 (RFC 1945)
* HTTP 1.1 became an oficial standard in 1997 (RFC 2616)

### SPDY

* Binary protocol worked on by Mike Belshe & Roberto Peon at Google
* Implementeed on Chrome & GFE server between 2009 & 2014
* Became the basic of HTTP/2

### HTTP/2

* Published in May 2015
* RFC 7540 Hypertext Transfer Protocol version 2
  * Describes the new internals of the protocol
  * Designed for low latency
* RFC 7541 Header Compression (HPACK)

### Implementations

* Apache 2.4.17
* Nginx 1.9.5
* Akamai ~2015
* cURL 7.38.0
* IE 11
* Edge 2
* Chrome 41
* Firefox 36
* Safari 9

# Features

### Binary Framing

* Similar to TCP packets
* Frames contain distinct 
* Frame are indexed

### Streams

* Bidirectional flow of bytes within a connection
* May carry one or more messages (frames)
* Have identifiers
* Can be prioritized

### Multiplexing

* Frames in different streams can be interleaved
* Solves Head-of-Line blocking

### Server Push

* Server knows content when needed
  * HTML: CSS, JS, etc
  * JSON: URIs, etc
* Server sends a PUSH_PROMISE frame
* Client can decide to accept frame or reset it
* Support:
  * Nginx

### TLS Only

* Not mandated by the standard
* Chrome & Firefox stated they will not support without TLS
* Performance issues balanced in single connection scenario
* [http://letsencrypt.org](http://letsencrypt.org)


[1]: https://twitter.com/aramonc
[2]: http://chimera.labs.oreilly.com/books/1230000000545/index.html
