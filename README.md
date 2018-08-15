## Usage
source code: https://github.com/galalelatfawy/cog_task 

### Bringing up the stack

Start the ELK stack by building and running with the following command:

```console
$ sudo sysctl -w vm.max_map_count=262144
$ docker-compose build && docker-compose up
```

accss this url 
[http://localhost:5601](http://localhost:5601)


### task list completion 
# ● Nginx for serving any web pages of your choice.
 after running the compose file you can access the nginx website http://localhost:8080/cognitev.jpg 

#● Enable Nginx caching and compression.
after running the compose file use the below commands


```console
$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/test.jpg
$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/test2.jpg
$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/cognitev.jpg
```

This will give you an output similar to the below:
galal@HQE7240:~/Desktop/task0$ curl -IL -H "accept-encoding: gzip" http://localhost:8080/cognitev.jpg
HTTP/1.1 200 OK
Server: nginx/1.15.1
Date: Wed, 15 Aug 2018 11:07:50 GMT
Content-Type: image/jpeg
Last-Modified: Wed, 15 Aug 2018 07:29:43 GMT
Connection: keep-alive
Vary: Accept-Encoding
ETag: W/"5b73d667-23e69"
Expires: Thu, 31 Dec 2037 23:55:55 GMT
Cache-Control: max-age=315360000
Content-Encoding: gzip

# From the above you will notice that 'Cache-Control' and 'Content-Encoding' are showing that cache is set with and expiray date and compression is using gzip.



# ● Elasticsearch where Nginx logs will be saved.

access the kibana web ui http://localhost:5601 

# ● docker compose
 please visit my github account: 
 https://github.com/galalelatfawy/cog_task 
