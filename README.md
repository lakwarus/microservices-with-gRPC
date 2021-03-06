# Microservices-with-grpc

Clone microservices-with-grpc git repo and follow the README.md instructions.

$ cd microservices-with-grpc

### running cart microservice
$ cd cart
$ ballerina run cart_service
[ballerina/http] started HTTP/WS listener 0.0.0.0:8080

### running order microservice
$ cd order
$ ballerina run order_service
[ballerina/grpc] started HTTP/WS listener 0.0.0.0:9090

### running checkout microservice
$ cd checkout
$ ballerina run checkout_service
[ballerina/grpc] started HTTP/WS listener 0.0.0.0:9091

### running stock microservice
$ cd stock
$ go run stock/server/main.go
Server is listening on 0.0.0.0:9090 ...
$ go run gateway/main.go 

### sample payload to test internal communication
$ ./order.sh
### sample curl command to test grpc-gateway
$ curl -X POST -d '{ "itemNumber":"item3", "quantity": 50 }' http://localhost:8081/api/v1/stock

Note: Ballerina code sample is implemented by using Swan Lake release

