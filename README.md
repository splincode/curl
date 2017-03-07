# curl
snippets

```
$ curl --cookie-jar "jsession.out" -s -X POST --data "{login=admin,password=avkcom.ru}" --verbose http://localhost:8282/blackbox/auth/login-check && echo "\n"


*   Trying 127.0.0.1...
* Connected to localhost (127.0.0.1) port 8282 (#0)
> POST /blackbox/auth/login-check HTTP/1.1
> Host: localhost:8282
> User-Agent: curl/7.47.0
> Accept: */*
> Content-Length: 32
> Content-Type: application/x-www-form-urlencoded
> 
* upload completely sent off: 32 out of 32 bytes
< HTTP/1.1 200 OK
< Date: Tue, 07 Mar 2017 09:22:47 GMT
* Added cookie JSESSIONID="1p67blono8nna1v1rubezwzcn2" for domain localhost, path /blackbox, expire 0
< Set-Cookie: JSESSIONID=1p67blono8nna1v1rubezwzcn2;Path=/blackbox
< Expires: Thu, 01 Jan 1970 00:00:00 GMT
< Content-Length: 7
< Server: Jetty(9.3.15.v20161220)
< 
* Connection #0 to host localhost left intact
Success\n

```

```
$ curl --cookie "jsession.out" -s -i -X GET --verbose http://localhost:8282/blackbox/api/step-get?id=1 && echo "\n"


*   Trying 127.0.0.1...
* Connected to localhost (127.0.0.1) port 8282 (#0)
> GET /blackbox/api/step-get?id=1 HTTP/1.1
> Host: localhost:8282
> User-Agent: curl/7.47.0
> Accept: */*
> Cookie: JSESSIONID=1p67blono8nna1v1rubezwzcn2
> 
< HTTP/1.1 200 OK
HTTP/1.1 200 OK
< Date: Tue, 07 Mar 2017 09:23:24 GMT
Date: Tue, 07 Mar 2017 09:23:24 GMT
< Date: Tue, 07 Mar 2017 09:23:24 GMT
Date: Tue, 07 Mar 2017 09:23:24 GMT
< Content-Type: application/json; charset=UTF-8
Content-Type: application/json; charset=UTF-8
< Server: Jetty(9.3.15.v20161220)
Server: Jetty(9.3.15.v20161220)
< Content-Length: 93
Content-Length: 93

< 
* Connection #0 to host localhost left intact
{"success":true,"data":{"id":1,"title":"Инициация создания запроса"}}\n

```
