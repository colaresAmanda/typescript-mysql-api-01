# Bookstore API
This repository contains the code for a simple Bookstore API implemented in TypeScript using the Express.js framework and MySQL as the database. The API provides endpoints to create and retrieve books.

## API Endpoints
### Create a Book
- Route: POST /create/book
- Controller Method: createBook
- Description: This endpoint allows you to create a new book by sending a POST request with the book's author and title in the request body. The data is then inserted into the MySQL database.
### Get a Book by ID
- Route: GET /get/book/:id
- Controller Method: getBookById
- Description: This endpoint retrieves a book by its ID. Simply include the book ID in the URL, and it will return the book's details.
### Get All Books
- Route: GET /get/books
- Controller Method: getAllBooks
- Description: This endpoint fetches all books from the database and returns a list of books.

## SQL script
```sql
CREATE DATABASE IF NOT EXISTS typescript_mysql_api;

USE typescript_mysql_api;

CREATE TABLE IF NOT EXISTS books (
    id INT AUTO_INCREMENT,
    author VARCHAR(255) NOT NULL,
    title VARCHAR(255) NOT NULL,
    PRIMARY KEY (id)
);
```

## How to Use
- Clone the repository to your local environment.
- Install the required dependencies using `npm install`.
- Set up a MySQL database and configure the database connection details in the `config/mysql.ts` file.
- Run the API using `sudo npx ts-node-dev source/server.ts`.
