# RESTful Web Services

This guide introduces the core concepts of **RESTful Web Services** in a beginner-friendly way. REST stands for **Representational State Transfer**, and it is a common way for applications to communicate over the web using **HTTP**.

A **RESTful Web Service** uses URLs (endpoints) and standard HTTP methods like **GET**, **POST**, **PUT**, and **DELETE** to perform actions such as reading, creating, updating, and deleting data.

---

# Introduction to REST Endpoints

A **REST endpoint** is simply a URL (like `/users` or `/products`) that represents a resource.  
For example, `/users` might represent all users, and `/users/1` might represent a single user with ID 1.

Each endpoint responds to a specific HTTP method such as **GET** or **POST**.  
These methods determine what action the endpoint performs.

---

# Creating REST Endpoint with @Path

The `@Path` annotation defines the **location** (path) of an endpoint in a RESTful application.  
Think of it as the “address” where a client can find your service.

For example, if you set `@Path("/users")`, it means that when a user visits `/users` in a browser or through an API client, they are communicating with that part of your service.

---

# Creating GET Endpoint with @GET

The **GET** method is used when a client wants to **retrieve data**.  
You use this method when you want to display or fetch information, such as a list of users or a specific product.

For example, when you open a website to view available products, that page is often powered by a GET request to fetch all product details from the server.

---

# Creating POST Endpoint with @POST

The **POST** method is used when you want to **add or create** new data.  
This is like submitting a form or signing up for a service — your information is sent to the server to be stored or processed.

For example, when you register on a website, your details are sent through a POST request.

---

# Creating PUT Endpoint with @PUT

The **PUT** method is used when you want to **update** existing data.  
It replaces an existing record with new information.

For example, if a user wants to update their profile information, a PUT request is used to send the new data to the server.

---

# Creating DELETE Endpoint with @DELETE

The **DELETE** method is used when you want to **remove** something from the server.  
For example, if a user wants to delete their account, the system uses a DELETE request to remove it from the database.

---

# Returning JSON with @Produces(MediaType.APPLICATION_JSON)

When the server sends data to the client, it must choose a format the client understands.  
One common format is **JSON (JavaScript Object Notation)** because it’s lightweight and easy for both humans and computers to read.

`@Produces(MediaType.APPLICATION_JSON)` tells the system to return data in JSON format.

---

# Consuming JSON with @Consumes(MediaType.APPLICATION_JSON)

When clients send data to the server, they also use JSON format.  
`@Consumes(MediaType.APPLICATION_JSON)` means the server can **receive and understand JSON data**.

For example, if a client sends `{ "name": "Rose", "age": 24 }`, the server reads and processes that data.

---

# Using @PathParam to Read URL Parameters

Sometimes, you need to extract a specific part of a URL to identify a resource — for example, `/users/10` means you want the user with ID 10.

`@PathParam` allows you to **read values directly from the URL path**.  
It’s like telling the program, “Get the number after `/users/` so we know which user to work with.”

---

# Using @QueryParam to Read Query Parameters

A **query parameter** is the part of a URL that comes after a question mark (`?`).  
For example, `/search?name=Rose` is a request to search for a user named Rose.

`@QueryParam` allows your service to **read these extra details** from the URL and use them to filter or customize results.

---

# Handling HTTP Headers with @HeaderParam

HTTP headers carry **extra information** with a request, like authentication tokens or content types.  
`@HeaderParam` allows you to read these headers and use them to perform tasks such as verifying users or identifying request types.

For example, a header might contain an API key that confirms the user is allowed to access certain data.

---

# Returning Custom HTTP Response Codes

Every time the server responds to a client, it includes a **status code**.  
These codes indicate whether the request succeeded or failed.

- **200 OK** – Everything worked fine.
- **201 Created** – A new resource was created successfully.
- **400 Bad Request** – Something was wrong with the request.
- **404 Not Found** – The resource could not be found.
- **500 Internal Server Error** – Something went wrong on the server.

Returning the correct code helps clients understand what happened with their request.

---

# Using Response Object in Endpoints

A **Response object** gives you control over what the server sends back.  
You can set the message, data, and even add headers.  
This helps you make your responses clear, structured, and meaningful.

For example, you can send a message like “User created successfully” along with a **201 Created** status code.

---

# Exception Handling with @ApplicationException

Sometimes, things go wrong — maybe the user doesn’t exist, or the server can’t process the request.  
An **exception** is an error that interrupts the normal flow of a program.

`@ApplicationException` allows developers to mark certain errors as application-level exceptions, meaning they can be handled and returned in a user-friendly way instead of crashing the system.

---

# Custom ExceptionMapper

An **ExceptionMapper** lets you define what happens when a specific type of error occurs.  
Instead of showing confusing technical messages, you can send clear responses like:

> "User not found" or "Invalid input provided."

It makes your API easier to understand and more professional.

---

# Combining Validation and Exception Handling

Validation ensures that users send **correct and complete data** to your system.  
For example, an email address must contain “@”, and an age cannot be negative.

When combined with exception handling, validation ensures that if a user sends invalid data, the system responds gracefully — telling them what went wrong instead of breaking.

This makes your web service **reliable, safe, and user-friendly**.

# Summary

In RESTful web services:

- **GET** retrieves data.
- **POST** creates new data.
- **PUT** updates existing data.
- **DELETE** removes data.
- **@Produces** and **@Consumes** control data formats (like JSON).
- **@PathParam**, **@QueryParam**, and **@HeaderParam** read information from the request.
- **Response objects**, **exception handling**, and **validation** improve clarity and stability.

Together, these concepts form the foundation for creating robust, scalable, and easy-to-use RESTful APIs.

I
