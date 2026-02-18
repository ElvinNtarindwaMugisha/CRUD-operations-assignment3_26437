## RESTful API Assignment – Product Management System
## Project Overview

This project is a Spring Boot RESTful API that implements full CRUD (Create, Read, Update, Delete) operations for managing products in an e-commerce–style system.
The application uses Spring Data JPA and PostgreSQL for data persistence and follows REST best practices.



## Project Structure
```
restfullApiAssignment
│
├── controller
│   └── ProductController.java
│
├── service
│   └── ProductService.java
│
├── repository
│   └── ProductRepository.java
│
├── modal
│   └── Product.java
│
├── RestfullApiAssignmentApplication.java
└── application.properties
```
 ## Features Implemented

* Add a new product

* Retrieve all products

* Retrieve a product by ID

* Update an existing product

* Delete a product

## PostgreSQL database integration

Automatic table creation using Hibernate

 Database Configuration

The application is connected to a PostgreSQL database.
```
application.properties
spring.datasource.url=jdbc:postgresql://localhost:5432/ecommerce_db
spring.datasource.username=postgres
spring.datasource.password=12345

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.datasource.driver-class-name=org.postgresql.Driver
```

 ## API Endpoints
* Create Product
POST /api/products/addProduct


Request Body (JSON):
```
{
  "id": 1001,
  "name": "Wireless Mouse",
  "description": "Bluetooth wireless mouse",
  "price": 25.99,
  "category": "Electronics",
  "stockQuantity": 100
}
```
* Get All Products
GET /api/products/getAll

* Get Product by ID
GET /api/products/get/{id}

* Update Product
PUT /api/products/update/{id}


Request Body (JSON):
```
{
  "name": "Wireless Mouse Pro",
  "description": "Upgraded mouse",
  "price": 35.99,
  "category": "Electronics",
  "stockQuantity": 80
}
```
* Delete Product
DELETE /api/products/delete/{id}

## Testing the API

All endpoints were tested using Postman

Requests and responses are exchanged in JSON format

Proper HTTP status codes are returned (200, 201, 404, 409)
