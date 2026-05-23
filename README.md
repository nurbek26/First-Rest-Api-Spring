# First Rest API Spring

## 1. Project Overview

This project is a simple REST API built using Spring Boot. It demonstrates a clean layered architecture using:

- Controller (API layer)
- Service (business logic)
- Repository (data access)
- Domain model
- DTOs (request/response)
- Mapper (object mapping)
- Exception handling
- Swagger UI documentation

The API allows creating, reading, updating and deleting Product objects and returning them as JSON.

---

## 2. Technologies & Dependencies

The project was created using Spring Initializr inside IntelliJ IDEA with:

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database
- Spring Boot DevTools
- Swagger / OpenAPI

---

## 3. Project Structure

The assignment requires the following package layout:

```text
firstrestapispring
├── product
│   ├── api
│   │   ├── request
│   │   │   ├── ProductRequest.java
│   │   │   └── UpdateProductRequest.java
│   │   ├── response
│   │   │   └── ProductResponse.java
│   │   └── ProductController.java
│   ├── domain
│   │   └── Product.java
│   ├── repository
│   │   └── ProductRepository.java
│   ├── service
│   │   └── ProductService.java
│   └── support
│       ├── exception
│       │   └── ProductNotFoundException.java
│       ├── ProductExceptionAdvisor.java
│       ├── ProductExceptionSupplier.java
│       └── ProductMapper.java
├── shared
│   └── api
│       └── response
│           └── ErrorMessageResponse.java
└── FirstRestApiSpringApplication.java
4. Step-by-Step Implementation
Step 1 — Create the project

The project was created in IntelliJ IDEA:

File → New → Project → Spring Initializr

Dependencies added:

Spring Web
Spring Data JPA
H2 Database
Spring Boot DevTools
Swagger / OpenAPI
Step 2 — Create the Domain Model

The Product class represents the main object in the application.

It contains:

id
name
constructor
getters and setters

This object is stored in the repository and returned in responses.

Step 3 — Create the Repository

The ProductRepository class is responsible for saving and reading products.

At this stage, the project uses a HashMap as a simple in-memory database.

The repository contains:

Map<Long, Product> map = new HashMap<>();
long counter = 1;

Main methods:

save(Product entity)
findById(Long id)
findAll()
deleteById(Long id)

The counter is used to generate product IDs.

---

### Step 4 — Create DTO Classes

DTO classes are used for request and response.

`ProductRequest` receives JSON data.

`ProductResponse` returns product data.

`UpdateProductRequest` is used for updating products.

---

### Step 5 — Create Mapper

`ProductMapper` converts objects:

- ProductRequest → Product
- Product → ProductResponse

The mapper helps keep the code clean.

---

### Step 6 — Create Service

`ProductService` contains business logic.

Responsibilities:

- create product
- find product
- update product
- delete product

The service uses:

- ProductRepository
- ProductMapper

---

### Step 7 — Create Controller

`ProductController` handles HTTP requests.

Endpoints:

- POST `/api/v1/products`
- GET `/api/v1/products/{id}`
- PUT `/api/v1/products/{id}`
- DELETE `/api/v1/products/{id}`

Swagger UI:

```text
http://localhost:8080/swagger-ui/index.html
```

---

## 5. Testing API

The API was tested using Swagger UI.

Example request:

```json
{
  "name": "First Product"
}
```

Example response:

```json
{
  "id": 1,
  "name": "First Product"
}
```

The application supports CRUD operations.

---

## 6. H2 Console

H2 console:

```text
http://localhost:8080/h2-console
```

JDBC URL:

```text
jdbc:h2:mem:testdb
```

---

## 7. Summary

This project demonstrates a simple REST API built with Spring Boot using layered architecture and CRUD operations.

## H2 Console

![H2 Console](screenshots/h2-console.png)
<img width="1919" height="1199" alt="image" src="https://github.com/user-attachments/assets/32457d1d-b48e-4ad6-bc76-56e4ce0415af" />
