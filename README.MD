# Jobs API

A RESTful API for managing job listings. Users can register, log in, and perform CRUD operations on job listings. This API is built using Node.js, Express, and MongoDB, with JWT-based authentication.

## Features

- **User Authentication**: Register and login users with email and password. Returns a JWT token for secure access.
- **Job Listings**: Create, read, update, and delete job listings. Only authenticated users can access their own job listings.
- **Security**: Secure routes using JWT authentication. Implements common security measures like rate limiting, helmet, and XSS protection.

## Technologies Used

- **Node.js**: JavaScript runtime for building the backend.
- **Express**: Web framework for handling HTTP requests and routing.
- **MongoDB**: NoSQL database for storing job listings and user information.
- **Mongoose**: MongoDB object modeling tool for working with MongoDB in Node.js.
- **JWT (JSON Web Tokens)**: For user authentication and session management.
- **bcryptjs**: For securely hashing and comparing passwords.
- **Helmet**: Security middleware to set HTTP headers for security.
- **Express-Async-Errors**: To handle asynchronous errors without boilerplate.
- **Cors**: For enabling Cross-Origin Resource Sharing (CORS).
- **XSS-Clean**: Middleware to prevent XSS (Cross-Site Scripting) attacks.
- **Express-Rate-Limit**: To prevent brute-force attacks by limiting the number of requests from a user in a given time period.

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Cauebf/jobs-api/tree/main
   cd jobs-api
   ```

2. Install dependencies:
   
   ```bash
   npm install
   ```

3. Set up your environment variables by creating a .env file in the root directory with the following content:

   ```bash
   MONGO_URI=your-mongodb-connection-uri
   JWT_SECRET=your-jwt-secret
   JWT_LIFETIME=1d
   PORT=3000
   ```

4. Run the application:

   ```bash
   npm start
   ```

The API will be accessible at http://localhost:3000/api/v1.

## API Documentation

You can access the full API documentation (Swagger) at the following endpoint:

   ```bash
   http://localhost:3000/api/v1/docs
   ```

Alternatively, you can view the Swagger YAML documentation in the swagger.yaml file in this repository.

## Security

All routes except /auth/register and /auth/login require a valid JWT token to be passed in the Authorization header:

   ```bash
   Authorization: Bearer <your-jwt-token>
   ```

## Contributing

If you would like to contribute to this project, feel free to open issues or submit pull requests.