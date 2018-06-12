# non-www to www
```
curl -vvIL site1.test --insecure
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
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Content-Length: 5
Content-Length: 5
< Content-Type: text/plain; charset=utf-8
Content-Type: text/plain; charset=utf-8

< 
* Connection #0 to host site1.test left intact
* Issue another request to this URL: 'https://site1.test:443/'
* Found bundle for host site1.test: 0x55c489819330 [can pipeline]
*   Trying 127.0.0.1...
* Connected to site1.test (127.0.0.1) port 443 (#1)
* found 148 certificates in /etc/ssl/certs/ca-certificates.crt
* found 597 certificates in /etc/ssl/certs
* ALPN, offering http/1.1
* SSL connection using TLS1.2 / ECDHE_RSA_AES_128_GCM_SHA256
* 	 server certificate verification SKIPPED
* 	 server certificate status verification SKIPPED
* 	 common name: site1.test (matched)
* 	 server certificate expiration date OK
* 	 server certificate activation date OK
* 	 certificate public key: RSA
* 	 certificate version: #3
* 	 subject: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 start date: Thu, 07 Jun 2018 10:21:25 GMT
* 	 expire date: Fri, 07 Jun 2019 10:21:25 GMT
* 	 issuer: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 compression: NULL
* ALPN, server accepted to use http/1.1
> HEAD / HTTP/1.1
> Host: site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 302 Found
HTTP/1.1 302 Found
< Location: https://www.site1.test/
Location: https://www.site1.test/
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Content-Length: 5
Content-Length: 5
< Content-Type: text/plain; charset=utf-8
Content-Type: text/plain; charset=utf-8

< 
* Connection #1 to host site1.test left intact
* Issue another request to this URL: 'https://www.site1.test/'
*   Trying 127.0.0.1...
* Connected to www.site1.test (127.0.0.1) port 443 (#2)
* found 148 certificates in /etc/ssl/certs/ca-certificates.crt
* found 597 certificates in /etc/ssl/certs
* ALPN, offering http/1.1
* SSL connection using TLS1.2 / ECDHE_RSA_AES_128_GCM_SHA256
* 	 server certificate verification SKIPPED
* 	 server certificate status verification SKIPPED
* 	 common name: site1.test (does not match 'www.site1.test')
* 	 server certificate expiration date OK
* 	 server certificate activation date OK
* 	 certificate public key: RSA
* 	 certificate version: #3
* 	 subject: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 start date: Thu, 07 Jun 2018 10:21:25 GMT
* 	 expire date: Fri, 07 Jun 2019 10:21:25 GMT
* 	 issuer: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 compression: NULL
* ALPN, server accepted to use http/1.1
> HEAD / HTTP/1.1
> Host: www.site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 200 OK
HTTP/1.1 200 OK
< Accept-Ranges: bytes
Accept-Ranges: bytes
< Content-Length: 547
Content-Length: 547
< Content-Type: text/html
Content-Type: text/html
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Etag: "5b1f9f69-223"
Etag: "5b1f9f69-223"
< Last-Modified: Tue, 12 Jun 2018 10:24:41 GMT
Last-Modified: Tue, 12 Jun 2018 10:24:41 GMT
< Server: nginx/1.13.12
Server: nginx/1.13.12

< 
* Connection #2 to host www.site1.test left intact

```


# www to non-www
```
curl -vvIL www.site1.test --insecure
* Rebuilt URL to: www.site1.test/
*   Trying 127.0.0.1...
* Connected to www.site1.test (127.0.0.1) port 80 (#0)
> HEAD / HTTP/1.1
> Host: www.site1.test
> User-Agent: curl/7.47asdasd.0
> Accept: */*
> 
< HTTP/1.1 302 Found
HTTP/1.1 302 Found
< Location: https://www.site1.test:443/
Location: https://www.site1.test:443/
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Content-Length: 5
Content-Length: 5
< Content-Type: text/plain; charset=utf-8
Content-Type: text/plain; charset=utf-8

< 
* Connection #0 to host www.site1.test left intact
* Issue another request to this URL: 'https://www.site1.test:443/'
* Found bundle for host www.site1.test: 0x55c489819330 [can pipeline]
*   Trying 127.0.0.1...
* Connected to www.site1.test (127.0.0.1) port 443 (#1)
* found 148 certificates in /etc/ssl/certs/ca-certificates.crt
* found 597 certificates in /etc/ssl/certs
* ALPN, offering http/1.1
* SSL connection using TLS1.2 / ECDHE_RSA_AES_128_GCM_SHA256
* 	 server certificate verification SKIPPED
* 	 server certificate status verification SKIPPED
* 	 common name: www.site1.test (matched)
* 	 server certificate expiration date OK
* 	 server certificate activation date OK
* 	 certificate public key: RSA
* 	 certificate version: #3
* 	 subject: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=www.site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 start date: Thu, 07 Jun 2018 10:21:25 GMT
* 	 expire date: Fri, 07 Jun 2019 10:21:25 GMT
* 	 issuer: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=www.site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 compression: NULL
* ALPN, server accepted to use http/1.1
> HEAD / HTTP/1.1
> Host: www.site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 302 Found
HTTP/1.1 302 Found
< Location: https://site1.test/
Location: https://site1.test/
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Content-Length: 5
Content-Length: 5
< Content-Type: text/plain; charset=utf-8
Content-Type: text/plain; charset=utf-8

< 
* Connection #1 to host site1.test left intact
* Issue another request to this URL: 'https://site1.test/'
*   Trying 127.0.0.1...
* Connected to site1.test (127.0.0.1) port 443 (#2)
* found 148 certificates in /etc/ssl/certs/ca-certificates.crt
* found 597 certificates in /etc/ssl/certs
* ALPN, offering http/1.1
* SSL connection using TLS1.2 / ECDHE_RSA_AES_128_GCM_SHA256
* 	 server certificate verification SKIPPED
* 	 server certificate status verification SKIPPED
* 	 common name: site1.test (does not match 'site1.test')
* 	 server certificate expiration date OK
* 	 server certificate activation date OK
* 	 certificate public key: RSA
* 	 certificate version: #3
* 	 subject: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 start date: Thu, 07 Jun 2018 10:21:25 GMT
* 	 expire date: Fri, 07 Jun 2019 10:21:25 GMT
* 	 issuer: C=IN,ST=MH,L=PUNE,O=GUGAL,OU=MAYKRAVSAFT,CN=site1.test,EMAIL=MAYKRAVSAFT@GUGAL.KOM
* 	 compression: NULL
* ALPN, server accepted to use http/1.1
> HEAD / HTTP/1.1
> Host: site1.test
> User-Agent: curl/7.47.0
> Accept: */*
> 
< HTTP/1.1 200 OK
HTTP/1.1 200 OK
< Accept-Ranges: bytes
Accept-Ranges: bytes
< Content-Length: 547
Content-Length: 547
< Content-Type: text/html
Content-Type: text/html
< Date: Tue, 12 Jun 2018 10:36:42 GMT
Date: Tue, 12 Jun 2018 10:36:42 GMT
< Etag: "5b1f9f69-223"
Etag: "5b1f9f69-223"
< Last-Modified: Tue, 12 Jun 2018 10:24:41 GMT
Last-Modified: Tue, 12 Jun 2018 10:24:41 GMT
< Server: nginx/1.13.12
Server: nginx/1.13.12

< 
* Connection #2 to host site1.test left intact

```