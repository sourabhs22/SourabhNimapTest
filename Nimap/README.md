# Spring Boot Category and Product CRUD

This project implements CRUD operations for `Category` and `Product` entities using Spring Boot with JPA and Hibernate. 

## Features

- CRUD operations for Category and Product
- One-to-Many relationship between Category and Products
- Pagination support for list APIs

## Prerequisites

- Java 17+
- Maven
- MySQL

## Setup

1. Clone the project.
2. Update `src/main/resources/application.properties` with your database credentials.
3. Run the application:
   ```bash
   mvn spring-boot:run
   ```

## APIs

### Category APIs

1. `GET /api/categories?page={page}` - Get all categories (paged)
2. `GET /api/categories/{id}` - Get category by ID
3. `POST /api/categories` - Create a new category
4. `PUT /api/categories/{id}` - Update category by ID
5. `DELETE /api/categories/{id}` - Delete category by ID

### Product APIs

1. `GET /api/products?page={page}` - Get all products (paged)
2. `GET /api/products/{id}` - Get product by ID
3. `POST /api/products` - Create a new product
4. `PUT /api/products/{id}` - Update product by ID
5. `DELETE /api/products/{id}` - Delete product by ID

## Database Schema

### Category
- `id` (Primary Key)
- `name` (String)
- `description` (String)

### Product
- `id` (Primary Key)
- `name` (String)
- `description` (String)
- `category_id` (Foreign Key)
