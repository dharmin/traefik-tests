```
$ curl -vvIL site1.test --insecure
* Rebuilt URL to: site1.test/
*   Trying 127.0.0.1...
* Connected to site1.test (127.0.0.1) port 80 (#0)
> HEAD / HTTP/1.1
> Host: site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 302 Found
HTTP/1.1 302 Found
< Location: https://site1.test:443/
Location: https://site1.test:443/
< Date: Thu, 07 Jun 2018 13:19:14 GMT
Date: Thu, 07 Jun 2018 13:19:14 GMT
< Content-Length: 5
Content-Length: 5
< Content-Type: text/plain; charset=utf-8
Content-Type: text/plain; charset=utf-8

< 
* Connection #0 to host site1.test left intact
* Issue another request to this URL: 'https://site1.test:443/'
* Found bundle for host site1.test: 0x5646563a1330 [can pipeline]
*   Trying 127.0.0.1...
* Connected to site1.test (127.0.0.1) port 443 (#1)
* found 148 certificates in /etc/ssl/certs/ca-certificates.crt
* found 597 certificates in /etc/ssl/certs
* ALPN, offering http/1.1
* SSL connection using TLS1.2 / ECDHE_RSA_AES_128_GCM_SHA256
* 	 server certificate verification SKIPPED
* 	 server certificate status verification SKIPPED
* 	 common name: TRAEFIK DEFAULT CERT (does not match 'site1.test')
* 	 server certificate expiration date OK
* 	 server certificate activation date OK
* 	 certificate public key: RSA
* 	 certificate version: #3
* 	 subject: CN=TRAEFIK DEFAULT CERT
* 	 start date: Thu, 07 Jun 2018 13:18:18 GMT
* 	 expire date: Fri, 07 Jun 2019 13:18:18 GMT
* 	 issuer: CN=TRAEFIK DEFAULT CERT
* 	 compression: NULL
* ALPN, server accepted to use http/1.1
> HEAD / HTTP/1.1
> Host: site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 301 Moved Permanently
HTTP/1.1 301 Moved Permanently
< Content-Length: 186
Content-Length: 186
< Content-Type: text/html
Content-Type: text/html
< Date: Thu, 07 Jun 2018 13:19:14 GMT
Date: Thu, 07 Jun 2018 13:19:14 GMT
< Location: https://site1.test/
Location: https://site1.test/
< Server: nginx/1.13.12
Server: nginx/1.13.12

< 
* Connection #1 to host site1.test left intact
* Issue another request to this URL: 'https://site1.test/'
* Found bundle for host site1.test: 0x5646563a1330 [can pipeline]
* Re-using existing connection! (#1) with host site1.test
* Connected to site1.test (127.0.0.1) port 443 (#1)
> HEAD / HTTP/1.1
> Host: site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 200 OK
HTTP/1.1 200 OK
< Accept-Ranges: bytes
Accept-Ranges: bytes
< Content-Length: 350
Content-Length: 350
< Content-Type: text/html
Content-Type: text/html
< Date: Thu, 07 Jun 2018 13:19:14 GMT
Date: Thu, 07 Jun 2018 13:19:14 GMT
< Etag: "5b18cb1d-15e"
Etag: "5b18cb1d-15e"
< Last-Modified: Thu, 07 Jun 2018 06:05:17 GMT
Last-Modified: Thu, 07 Jun 2018 06:05:17 GMT
< Server: nginx/1.13.12
Server: nginx/1.13.12

< 
* Connection #1 to host site1.test left intact

```