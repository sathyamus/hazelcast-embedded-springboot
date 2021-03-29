

Running the Sample Application

Run the application using Maven on a terminal:

mvn spring-boot:run -Dspring-boot.run.jvmArguments="-Dserver.port=8080"

Then rerun the application on another terminal. 
Note that you need to set a different value for the server.port.

mvn spring-boot:run -Dspring-boot.run.jvmArguments="-Dserver.port=8081"



See the guide [here](https://guides.hazelcast.org/hazelcast-embedded-springboot).