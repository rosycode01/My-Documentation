# My Quarkus Journey & Roadmap

## Connect with Me

You can reach out or follow my work here:

[![GitHub](https://img.shields.io/badge/GitHub-rosycode01-black?logo=github)](https://github.com/rosycode01)  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Rose%20Muragu-blue?logo=linkedin)](https://www.linkedin.com/in/rosycode01/)  
[![Email](https://img.shields.io/badge/Email-rosemuragu4@gmail.com-red?logo=gmail)](mailto:rosemuragu4@gmail.com)

---

## Becoming a Backend Engineer

From the start of my software development journey, I realized the value of being a **detailed, hands-on backend engineer**.  
In the world of business and enterprise software, backend engineers are the backbone of any system — responsible for ensuring data integrity, seamless integrations, and robust performance.

I firmly believe that **specialization is key**. Focusing on a niche allows developers to deepen their expertise, make impactful contributions, and become highly sought-after professionals.  
For me, the business and enterprise sector was the natural choice, where scalable, efficient, and maintainable systems are critical.

---

## Why I Chose Quarkus

After deciding to focus on enterprise applications, I explored different backend frameworks.  
I chose **Quarkus (Java)** because it is **tailored for cloud-native, high-performance, and reactive applications** — a game-changer for business software.

**Why Quarkus is important for developers in the business sector:**

- **High performance** with minimal memory footprint and fast startup times
- **Reactive programming support**, allowing scalable and efficient systems
- **Cloud-native readiness**, simplifying containerization, microservices, and deployment
- **Developer productivity**, with live reload, dev UI, and robust extension ecosystem

In short, Quarkus provides **speed, scalability, and maintainability**, all of which are crucial in enterprise-grade applications.

---

## How I Went About Learning Quarkus

I am a **hands-on learner**, so my approach was to **learn, practice, and build simultaneously**.  
For each concept in the roadmap, I would first study it, then immediately apply it in a practical context to reinforce my understanding.

Alongside following the roadmap, I **built a Wholesale CRM application**. This project allowed me to:

- Cement what I learned in real-world scenarios
- Apply Quarkus features like REST endpoints, persistence, dependency injection, and reactive messaging
- Gain confidence in designing, developing, and deploying enterprise-grade applications

This approach ensured that my learning was **practical, tangible, and directly applicable** to real business solutions.

---

## My Quarkus Roadmap

To systematically learn Quarkus and master enterprise backend development, I decided to follow a **step-by-step roadmap**, broken down into bite-sized topics to study in 30-minute sessions.

<details>
<summary>Click to Expand Full Quarkus Roadmap</summary>

### Quarkus Fundamentals

1. What is Quarkus
2. Benefits of Quarkus
3. Quarkus architecture overview
4. Difference between Quarkus and Spring Boot
5. Quarkus reactive vs imperative programming
6. Quarkus native image concept
7. Quarkus container-first approach
8. Understanding Quarkus build time vs runtime

### Setup and Project Creation

9. Installing Quarkus SDK
10. Setting up IDE for Quarkus
11. Installing VS Code Quarkus plugin
12. Installing IntelliJ Quarkus plugin
13. Creating a new Quarkus project with Maven
14. Understanding Quarkus project folder structure
15. Exploring src main java folder
16. Exploring resources folder
17. Understanding pom.xml
18. Running Quarkus app using mvn quarkus:dev
19. Live reload feature in Quarkus
20. Packaging Quarkus app with mvn package

### Dependency Injection and Beans

21. Introduction to Dependency Injection
22. Using @Inject annotation
23. Using @ApplicationScoped annotation
24. Using @Singleton annotation
25. Using @RequestScoped annotation
26. Using @Dependent scope
27. Understanding bean lifecycle
28. Producing custom beans with @Produces
29. Qualifiers for bean injection
30. Injecting configuration properties into beans

### RESTful Web Services

31. Introduction to REST endpoints
32. Creating REST endpoint with @Path
33. Creating GET endpoint with @GET
34. Creating POST endpoint with @POST
35. Creating PUT endpoint with @PUT
36. Creating DELETE endpoint with @DELETE
37. Returning JSON with @Produces MediaType.APPLICATION_JSON
38. Consuming JSON with @Consumes MediaType.APPLICATION_JSON
39. Using @PathParam to read URL parameters
40. Using @QueryParam to read query parameters
41. Handling HTTP headers with @HeaderParam
42. Returning custom HTTP response codes
43. Using Response object in endpoints
44. Exception handling with @ApplicationException
45. Custom ExceptionMapper
46. Combining validation and exception handling

### Validation

47. Introduction to input validation
48. Validating with @NotNull
49. Validating with @Size
50. Validating with @Email
51. Validating with @Pattern
52. Validating numeric ranges with @Min and @Max
53. Grouped validations
54. Custom validation annotations
55. Handling validation errors in REST endpoints

### Persistence with JPA and Hibernate

56. Introduction to Hibernate ORM
57. Adding database dependency for PostgreSQL
58. Adding database dependency for MySQL
59. Creating Entity class with @Entity
60. Using @Id for primary key
61. Using @GeneratedValue for auto IDs
62. Mapping columns with @Column
63. Mapping table names with @Table
64. One-to-One relationship with @OneToOne
65. One-to-Many relationship with @OneToMany
66. Many-to-One relationship with @ManyToOne
67. Many-to-Many relationship with @ManyToMany
68. Creating Panache repository
69. Using CRUD methods in Panache repository
70. Persisting an entity
71. Fetching entities with findAll
72. Fetching entity by ID
73. Updating entities
74. Deleting entities
75. Writing custom queries with Panache

### Configuration

76. Introduction to application.properties
77. Setting basic configuration values
78. Using dev profile
79. Using test profile
80. Using prod profile
81. Reading environment variables
82. Overriding properties with env variables
83. Injecting config values with @ConfigProperty
84. Creating custom config classes
85. Runtime vs build time configuration

### Reactive Programming

86. Introduction to reactive programming
87. Understanding Uni type
88. Understanding Multi type
89. Reactive REST endpoint with Uni
90. Reactive REST endpoint with Multi
91. Combining Uni and Multi
92. Error handling in reactive endpoints
93. Integrating reactive persistence

### REST Client

94. Introduction to REST client
95. Creating REST client with @RestClient
96. Calling external REST APIs
97. Handling response errors in REST client
98. Using REST client with JSON mapping
99. REST client configuration properties

### Messaging

100. Introduction to reactive messaging
101. Producing Kafka events
102. Consuming Kafka events
103. Using @Channel annotation
104. Configuring channels in application.properties
105. Handling messages asynchronously

### Health and Metrics

106. Introduction to health checks
107. Creating health check with @Health
108. Liveness and readiness probes
109. Introduction to metrics
110. Using @Gauge annotation
111. Using @Timed annotation
112. Custom metrics with MicroProfile

### Security

113. Introduction to security
114. Securing endpoints with roles
115. Using @RolesAllowed annotation
116. JWT authentication basics
117. Quarkus OIDC extension
118. Using Keycloak with Quarkus
119. OAuth2 authentication
120. Securing REST clients

### GraphQL

121. Introduction to GraphQL
122. Creating GraphQL endpoint
123. Query resolvers
124. Mutation resolvers
125. Using GraphQL schema files

### Caching

126. Introduction to caching
127. Using @CacheResult
128. Using @CacheInvalidate
129. Using @CacheKey annotation
130. Configuring cache expiration

### Scheduling and Jobs

131. Introduction to scheduling
132. Using @Scheduled annotation
133. Scheduling at fixed intervals
134. Scheduling with cron expressions
135. Dynamic scheduling

### Testing

136. Writing unit tests with JUnit
137. Using @QuarkusTest annotation
138. Mocking beans with @InjectMock
139. Integration testing
140. Using REST Assured for REST testing
141. Testing database with Panache

### Native Image and Deployment

142. Introduction to native image
143. Building native executable
144. Optimizing native image
145. Understanding containerization
146. Dockerizing Quarkus application
147. Deploying Quarkus app to Docker
148. Deploying Quarkus app to Kubernetes
149. Deploying Quarkus app to OpenShift
150. Quarkus cloud-native best practices

### Extensions and Advanced Concepts

151. Using Quarkus extensions
152. Installing extensions with Maven
153. Reactive messaging extension
154. RESTEasy Reactive extension
155. Hibernate ORM Panache extension
156. GraphQL extension
157. Kafka extension
158. Security extension
159. Dev UI extension
160. Quarkus Dev Services for databases

### Observability and Monitoring

161. Logging in Quarkus
162. Structured logging
163. Distributed tracing
164. Using OpenTelemetry
165. Monitoring metrics via Prometheus
166. Exposing health endpoints
167. Exposing metrics endpoints

</details>
