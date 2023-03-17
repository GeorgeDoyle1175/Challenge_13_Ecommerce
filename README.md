# Overview

This code contains a set of Express routes and Sequelize models for a basic e-commerce application. The application allows users to create and view products, as well as add and remove product tags.

## Routes
The following routes are included in the code:

## GET /api/products
This route retrieves all products from the database and returns them as JSON.

## GET /api/products/:id
This route retrieves a single product from the database by its ID and returns it as JSON.

## POST /api/products
This route creates a new product in the database. The request body should include the following fields:

product_name (string)
price (float)
stock (integer)
tagIds (array of integers)
If the tagIds field is provided, the corresponding tags will be associated with the new product.

## PUT /api/products/:id
This route updates an existing product in the database by its ID. The request body can include any of the following fields:

product_name (string)
price (float)
stock (integer)
tagIds (array of integers)
If the tagIds field is provided, the corresponding tags will be associated with the updated product. If any tags are removed, they will be disassociated from the product.

## DELETE /api/products/:id
This route deletes an existing product from the database by its ID.

## GET /api/tags
This route retrieves all tags from the database and returns them as JSON.

## GET /api/tags/:id
This route retrieves a single tag from the database by its ID and returns it as JSON.

## POST /api/tags
This route creates a new tag in the database. The request body should include the following field:

tag_name (string)
PUT /api/tags/:id
This route updates an existing tag in the database by its ID. The request body should include the following field:

tag_name (string)
DELETE /api/tags/:id
This route deletes an existing tag from the database by its ID.

## Models
The following Sequelize models are included in the code:

Product
product_name (string)
price (float)
stock (integer)
Tag
tag_name (string)
ProductTag
product_id (integer)
tag_id (integer)
Product and Tag have a many-to-many relationship through ProductTag.

Error Handling
If any errors occur during a route's execution, a 400 status code will be returned along with a JSON object containing an error message.

## Dependencies
The following dependencies are required to run the code:

## Express
Sequelize
MySQL2
Running the Code
To run the code, follow these steps:

Install the required dependencies using npm install.
Create a MySQL database called ecommerce_db.
Set your MySQL username and password as environment variables named DB_USER and DB_PASSWORD, respectively.
Start the server using npm start.
Once the server is running, you can access the routes using a tool like Postman or by sending HTTP requests from your own application.

https://youtu.be/YOtVWlLTSMQ
