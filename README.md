# weather_reactive

Technologies:

- Spring Boot (REST)
- Spring WebFlux

Annotations:

- @Autowired
- @GetMapping
- @PathVariable
- @RestController
- @Service
- @SpringBootApplication

Description:

- The application demonstrates usage of reactive approach in web development.


- Cornerstone of reactive programming is operations with streams of data that allows to manipulate the received data 
at once not waiting for the complete receipt (of the rest of data) thus saving time and resources. This principle 
can be used in chats, broker platforms, and auctions.


- The application uses in-memory HashMap to store the data for simplicity. The domain model is Weather. The Controller 
has the mapping to request all Weather objects, find the one by id, find the hottest one, as well as find the ones 
that hotter than some value.
  

- Mono is a stream that consists of one element or the empty one. Flux is a stream that consists of number of elements 
or the empty one. The mappings return either Mono or Flux. Those that return Flux have an Annotation attribute 
"produces" that is initialized with MediaType.TEXT_EVENT_STREAM_VALUE that will force a browser to switch into the
reactive mode. Also, the delay interval is set up in the Flux objects to simulate a service with long loading.
  
