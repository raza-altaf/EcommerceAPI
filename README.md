# ECommerceAPI

This E-commerce API is built using Node.js and MongoDB to provide a seamless experience for managing product data. It allows users to retrieve a list of products, create new products, delete existing products, and update product quantities.

## Getting Started

### Prerequisites

Make sure you have Node.js and MongoDB installed on your system.

### Installation

1. Run the following command in the project directory to initialize the project:

   ```bash
   npm init
   ```

2. Start the server using the command:

   ```bash
   node app.js
   ```

3. Open Postman to interact with the API.

## Usage

### Retrieving Products

1. Make a GET request to the following endpoint:

   ```
   GET localhost:3000/products
   ```

   This will display a list of available products.

### Creating a New Product

1. Start the server using:

   ```bash
   node app.js
   ```

2. Open Postman and make a POST request to:

   ```
   POST localhost:3000/products/create
   ```

3. In the Body tab, select x-www-form-urlencoded and add `name` and `quantity` as keys with desired values.

4. Click Send. If you receive the message "New product added successfully," the product is created.

### Deleting a Product

1. Copy the Object ID of the product you want to delete.

2. Make a DELETE request to:

   ```
   DELETE localhost:3000/products/{objectID}
   ```

   Replace `{objectID}` with the copied ID. You will receive a "Deleted successfully" message.

### Updating Product Quantity

1. Copy the Object ID of the product you want to update.

2. Make a POST request to:

   ```
   POST localhost:3000/products/{objectID}/update_quantity/?number={x}
   ```

   Replace `{objectID}` with the copied ID and `{x}` with the desired quantity change. You will receive a message containing the updated product details.

## Tech Stack

- Node.js
- MongoDB

## Contribution

Contributions are welcome! If you find a bug or have an idea for an improvement, feel free to open an issue or submit a pull request.
