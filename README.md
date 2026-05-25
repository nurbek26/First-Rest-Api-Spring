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

Screenshot:<img width="1919" height="1128" alt="image" src="https://github.com/user-attachments/assets/5ad05fa1-d30e-46ca-aef0-63ee0a752333" />


Find Product

Response:

{
  "id": 1,
  "name": "First Product"
}

Screenshot: <img width="1918" height="1197" alt="Screenshot 2026-05-23 113252" src="https://github.com/user-attachments/assets/bbba6390-5fd5-4bdb-90c8-5c8795443939" />


Update Product

Response:

{
  "id": 1,
  "name": "Updated Product"
}

Screenshot: <img width="1918" height="1198" alt="Screenshot 2026-05-23 113748" src="https://github.com/user-attachments/assets/96b7c10b-1134-45d6-b858-93ef6664e7da" />


Delete Product

Status:

204 No Content

Screenshot: <img width="1918" height="1198" alt="Screenshot 2026-05-23 113619" src="https://github.com/user-attachments/assets/8062c05f-833e-4395-8f27-459d6216ad2e" />


Product Not Found

Response:

{
  "message": "Product with 1 not found"
}

Screenshot: <img width="1918" height="1198" alt="Screenshot 2026-05-23 113748" src="https://github.com/user-attachments/assets/d3597d1e-be1f-4c30-ad4d-b3fda205ee36" />


6. Summary

This project demonstrates a simple REST API built with Spring Boot using layered architecture and CRUD operations.

Swagger UI:

http://localhost:8080/swagger-ui/index.html
