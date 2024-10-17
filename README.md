
# Library Books Management API

## Overview

The **Book Management API** is a Spring Boot application designed to provide a comprehensive solution for managing books. This API allows users to create, update, delete, and retrieve book information using their ISBN. It also includes integration and unit tests to ensure the reliability and functionality of the services.

## Features

- Create new books
- Retrieve details of a specific book by ISBN
- Update existing book information
- Delete books from the database
- Integration and unit tests included

## Technologies Used

- Spring Boot
- Spring Data JPA
- H2 Database (for testing purposes)
- Maven

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 11 or higher
- Apache Maven
- IDE (e.g., IntelliJ IDEA, Eclipse)

### Clone the Repository

```bash
git clone https://github.com/yourusername/book-management-api.git
cd book-management-api
```

### Build the Project

To build the project, run the following command:

```bash
mvn clean install
```

### Run the Application

You can run the application using the following command:

```bash
mvn spring-boot:run
```

Alternatively, you can run the generated JAR file:

```bash
java -jar target/book-management-api-0.0.1-SNAPSHOT.jar
```

## API Endpoints

### 1. Get All Books
- **Endpoint**: `GET /books`
- **Description**: Retrieves a list of all books.

### 2. Get Book by ID
- **Endpoint**: `GET /book/{isbn}`
- **Description**: Retrieves the details of a specific book by its ISBN.
- **Path Parameters**: 
  - `isbn` (string): The ISBN of the book to retrieve.

### 3. Add a New Book
- **Endpoint**: `POST /books`
- **Description**: Adds a new book to the collection.
- **Request Body**:
  ```json
  {
      "isbn": "1234567890123",
      "title": "Book Title",
      "author": "Author Name",
      "publishedDate": "2024-01-01",
      "price": 29.99
  }
  ```

### 4. Update a Book
- **Endpoint**: `PUT /books`
- **Description**: Updates an existing book's information.
- **Request Body**:
  ```json
  {
      "isbn": "1234567890123",
      "title": "Updated Book Title",
      "author": "Updated Author Name",
      "publishedDate": "2024-01-01",
      "price": 24.99
  }
  ```

### 5. Delete a Book
- **Endpoint**: `DELETE /books/{isbn}`
- **Description**: Deletes a book from the collection.
- **Path Parameters**: 
  - `isbn` (string): The ISBN of the book to delete.

## Testing

The project includes integration and unit tests. You can run the tests using the following command:

```bash
mvn test
```

