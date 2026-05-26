# First Rest API Spring

## 1. Project Overview

This project is a simple REST API built using Spring Boot.

The application uses layered architecture:

- Controller
- Service
- Repository
- DTO
- Mapper

The API allows creating, finding, updating and deleting Product objects.

---

## 2. Technologies

The project was created using:

- Java
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 Database
- Swagger UI

---

## 3. Project Structure

```text
firstrestapispring
├── product
│   ├── api
│   ├── domain
│   ├── repository
│   ├── service
│   └── support
├── shared
└── FirstRestApiSpringApplication.java
4. Implementation
Step 1 — Create Project

The project was created in IntelliJ IDEA using Spring Initializr.

Dependencies added:

Spring Web
Spring Data JPA
H2 Database
Swagger UI
Step 2 — Create Product Class

The Product class represents the main object in the application.

Fields:

id
name
Step 3 — Create Repository

ProductRepository stores products using HashMap.

Main methods:

save()
findById()
findAll()
deleteById()
Step 4 — Create DTO Classes

DTO classes are used for request and response.

ProductRequest receives JSON data.

ProductResponse returns product data.

UpdateProductRequest is used for updating products.

Step 5 — Create Mapper

ProductMapper converts objects:

ProductRequest → Product
Product → ProductResponse
Step 6 — Create Service

ProductService contains business logic.

Responsibilities:

create product
find product
update product
delete product
Step 7 — Create Controller

ProductController handles HTTP requests.

Endpoints:

POST /api/v1/products
GET /api/v1/products/{id}
GET /api/v1/products
PUT /api/v1/products/{id}
DELETE /api/v1/products/{id}

5. API Examples
Create Product

Request:

{
  "name": "First Product"
}

Response:

{
  "id": 1,
  "name": "First Product"
}

<img width="1919" height="1128" alt="post png" src="https://github.com/user-attachments/assets/1911fbc2-e39f-4ffe-adbb-cc6d085474b9" />



Find Product

Response:

{
  "id": 1,
  "name": "First Product"
}

<img width="1918" height="1197" alt="get png" src="https://github.com/user-attachments/assets/53b99908-fee4-41a1-a203-c2c11a3aa557" />




Update Product

Response:

{
  "id": 1,
  "name": "Updated Product"
}

<img width="1918" height="1193" alt="put png" src="https://github.com/user-attachments/assets/bc6c7633-6e4d-4487-a9fe-3e4552133911" />



Delete Product

Status:

204 No Content


![Delete Product](https://github.com/user-attachments/assets/11871310-6f79-4180-9321-e9aaed390f51)


Product Not Found

Response:

{
  "message": "Product with 1 not found"
}

<img width="1918" height="1198" alt="error png" src="https://github.com/user-attachments/assets/19f0b1c7-64d9-44bd-8904-4ad34f534ef4" />



6. Summary

This project demonstrates a simple REST API built with Spring Boot using layered architecture and CRUD operations.

Swagger UI:

http://localhost:8080/swagger-ui/index.html
