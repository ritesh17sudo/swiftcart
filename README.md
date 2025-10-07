# SwiftCart

This is a MERN stack ecommerce application named SwiftCart.

## Project Overview

SwiftCart is a fully functional ecommerce platform built with the MERN stack. It provides a comprehensive set of features, including user authentication, product and category management, product search and filtering, and payment processing through Braintree.

## Technologies Used

*   **MongoDB**: NoSQL database for storing product and user data.
*   **Express.js**: Backend framework for building the RESTful API.
*   **React.js**: Frontend library for building the user interface.
*   **Node.js**: JavaScript runtime for the backend.

## Getting Started

### Prerequisites

*   Node.js and npm installed
*   MongoDB installed and running

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/your-username/swiftcart.git
    ```
2.  Install server and client dependencies:
    ```bash
    npm install && npm install --prefix client
    ```

### Running the Application

Start the backend and frontend servers concurrently:
```bash
npm run dev
```

The application will be available at `http://localhost:3000`.

## API Endpoints

### Authentication

- `POST /api/v1/auth/register`: Register a new user.
- `POST /api/v1/auth/login`: Login a user.
- `POST /api/v1/auth/forgot-password`: Request a password reset.
- `GET /api/v1/auth/user-auth`: Check if a user is authenticated.
- `GET /api/v1/auth/admin-auth`: Check if a user is an admin.
- `PUT /api/v1/auth/profile`: Update user profile.
- `GET /api/v1/auth/orders`: Get orders for the authenticated user.
- `GET /api/v1/auth/all-orders`: Get all orders (admin only).
- `PUT /api/v1/auth/order-status/:orderId`: Update order status (admin only).

### Categories

- `POST /api/v1/category/create-category`: Create a new category (admin only).
- `PUT /api/v1/category/update-category/:id`: Update a category (admin only).
- `GET /api/v1/category/get-category`: Get all categories.
- `GET /api/v1/category/single-category/:slug`: Get a single category by its slug.
- `DELETE /api/v1/category/delete-category/:id`: Delete a category (admin only).

### Products

- `POST /api/v1/product/create-product`: Create a new product (admin only).
- `PUT /api/v1/product/update-product/:pid`: Update a product (admin only).
- `GET /api/v1/product/get-product`: Get all products.
- `GET /api/v1/product/get-product/:slug`: Get a single product by its slug.
- `GET /api/v1/product/product-photo/:pid`: Get a product's photo.
- `DELETE /api/v1/product/delete-product/:pid`: Delete a product (admin only).
- `POST /api/v1/product/product-filters`: Filter products based on criteria.
- `GET /api/v1/product/product-count`: Get the total number of products.
- `GET /api/v1/product/product-list/:page`: Get a paginated list of products.
- `GET /api/v1/product/search/:keyword`: Search for products.
- `GET /api/v1/product/related-product/:pid/:cid`: Get related products.
- `GET /api/v1/product/product-category/:slug`: Get products by category.

### Payments

- `GET /api/v1/braintree/token`: Get a Braintree client token.
- `POST /api/v1/braintree/payment`: Process a payment.
