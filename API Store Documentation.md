API Store Documentation

This API was built independently to manage and retrieve product data efficiently. Below are the details of its setup, routes, and usage.![ref1]

**Table of Contents**

1. Overview
1. Getting Started
   1. Requirements
   1. Installation
   1. Running the Server
1. Routes
- **GET** /api/v1/products
- **GET** /api/v1/products/static
4. Models
4. Error Handling
4. Examples
4. Credits![ref1]
1. **Overview**

The **API Store** allows you to fetch, filter, and manage product data. It supports features like querying for featured products and retrieving all products statically.![ref1]

2. **Getting Started**

**Requirements**

- **Node.js** (v16+ recommended)
- **MongoDB** (Atlas or Local)
- Dependencies (see package.json)

**Installation**

1. **Clone the repository:**

git clone <repository-url> cd API\_Store![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.002.png)

2. **Install dependencies:**

npm install![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.003.png)

3. **Create a .env file in the root directory with the following variables:**

MONGO\_URI=your\_mongo\_connection\_string PORT=![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.004.png)5000

**Running the Server**

npm start![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.005.png)![ref1]

3. **Routes**

**GET /api/v1/products**

- **Description**: Retrieves all products from the database.
- **Parameters**:
- **featured** (optional): Filters products by the featured flag (true or false).
- **Response**:

{![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.006.png)

"products": [

{

"\_id": "product\_id", "name": "Product Name", "price": 100, "featured": true, "rating": 4.5

}

]![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.007.png)

}![ref1]

**GET** /api/v1/products/static

- **Description**: Fetches all products statically where featured is set to true.
- **Response**:

{![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.008.png)

"products": [

{

"\_id": "product\_id", "name": "Product Name", "price": 100, "featured": true

}

],

"rating": 5.0

}![ref1]

4. **Models**

**Product Model**

The Product model has the following fields:

- name (string)
- price (number)
- featured (boolean)
- rating (number)![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.009.png)
5. **Error Handling**

Errors are handled gracefully with appropriate status codes and messages. Example:

- 500 Internal Server Error: Database or server issue.
- 404 Not Found: Invalid route.![ref1]
6. **Examples**

**Fetch All Products**

- **Request**:

GET /api/v1/products![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.010.png)

- **Response**:

{![](Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.011.png)

"products": [] }![ref1]

7. **Credits**

This API was independently developed by **Gustavo** / **Darkpwd**.

[ref1]: Aspose.Words.a3f10385-2578-4d0c-92bb-41339d921047.001.png
