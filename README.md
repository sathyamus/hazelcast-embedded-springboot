
# Hazelcast Running the Sample Application

-> Run the application using Maven on a terminal:

`
mvn spring-boot:run -Dspring-boot.run.jvmArguments="-Dserver.port=8080"
`

Then rerun the application on another terminal. 
Note that you need to set a different value for the server.port.

`
mvn spring-boot:run -Dspring-boot.run.jvmArguments="-Dserver.port=8081"
`


-> Issue HTTP requests to put and get data back. 
Run the following command to put the data into Hazelcast distributed map:

`
curl --data "key=key1&value=hazelcast" "localhost:8080/put"
`

You will see the value in the output. 
Then run the command below to get the data back. 
Please note that the call is made to the other application instance:

`
curl "localhost:8081/get?key=key1"
`

Again, you will see the value in the output since the data is distributed among Hazelcast cluster instances and can be accessed from any of them.

Verify the logs, where you can see from which instance is putting the key and value, which instance is retrieving them.
As the cache is distributed, it can be accessed from any instance, as said above.

See the guide [here](https://guides.hazelcast.org/hazelcast-embedded-springboot).
