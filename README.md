# Remote-Procedure-Call

To launch the application, either right-click the public static void main in PayRollApplication and select Run from your IDE, or:

Spring Initializr uses maven wrapper so type this:

$ ./mvnw clean spring-boot:run
Alternatively using your installed maven version type this:

$ mvn clean spring-boot:run
When the app starts, we can immediately interrogate it.

$ curl -v localhost:8080/employees
This will yield:

*   Trying ::1...
* TCP_NODELAY set
* Connected to localhost (::1) port 8080 (#0)
> GET /employees HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/7.54.0
> Accept: */*
>
< HTTP/1.1 200
< Content-Type: application/json;charset=UTF-8
< Transfer-Encoding: chunked
< Date: Thu, 09 Aug 2018 17:58:00 GMT
<
* Connection #0 to host localhost left intact
[{"id":1,"name":"Bilbo Baggins","role":"burglar"},{"id":2,"name":"Frodo Baggins","role":"thief"}]
