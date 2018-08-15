## Usage

### Bringing up the stack

Start the ELK stack by building and running with the following command:

```console
$ sudo sysctl -w vm.max_map_count=262144
$ docker-compose build && docker-compose up
```

accss this url 
[http://localhost:5601](http://localhost:5601)

### Checking gZip Compression and Caching

After the ELK stack has started you can use the following command in your terminal:

```console
$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/test.jpg
```

This will give you an output similar to the below:
galal@HQE7240:~/Desktop/task0$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/test.jpg
HTTP/1.1 200 OK
Server: nginx/1.15.1
Date: Wed, 15 Aug 2018 06:39:51 GMT
Content-Type: image/jpeg
Last-Modified: Mon, 13 Nov 2017 19:56:30 GMT
Connection: keep-alive
Vary: Accept-Encoding
ETag: W/"5a09f8ee-27621"
Expires: Thu, 31 Dec 2037 23:55:55 GMT
Cache-Control: max-age=315360000
Content-Encoding: gzip


From the above you will notice that 'Cache-Control' and 'Content-Encoding' are showing that cache is set with and expiray date and compression is using gzip.
