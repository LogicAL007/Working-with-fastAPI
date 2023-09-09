

# FastAPI REST API with Docker

This project is a simple REST API built using FastAPI and docker. It provides endpoints for managing customers and invoices.

## Features

- CRUD operations for customers and invoices.
- Containerized FastAPI application using Docker.
- Fake in-memory database storage using Python dictionaries.
- Defined Pydantic models for validation and serialization.

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop)
- [Git](https://git-scm.com/)

### Installation

1. Clone the repository:

   ```bash
   git clone [URL_OF_YOUR_GITHUB_REPOSITORY] Working-with-fastAPI
   cd Working-with-fastAPI
   ```

   Make sure to replace `[URL_OF_YOUR_GITHUB_REPOSITORY]` with the actual URL of your repository.

2. Build the Docker image:

   ```bash
   docker build -t fastapi_image .
   ```
<img width="867" alt="Screenshot 2023-09-09 040827" src="https://github.com/LogicAL007/Working-with-fastAPI/assets/122959675/0444ebb8-3af9-471f-b982-6c2a74c85b71">

3. Run the container:

   ```bash
   docker run -d -p 8000:80 fastapi_image
   ```
<img width="953" alt="Screenshot 2023-09-09 040808" src="https://github.com/LogicAL007/Working-with-fastAPI/assets/122959675/0d56389d-9825-4ca9-b4fc-0e497131b2c3">

4. Visit `http://localhost:8000` in your browser to see the API in action.

## API Endpoints

Here's a quick overview of the available endpoints:

- `GET /`: Base URL which returns a welcome message.
- `POST /customer`: Create a new customer.
- `GET /customer/{customer_id}`: Fetch details of a specific customer by their ID.
- `POST /customer/{customer_id}/invoice`: Create a new invoice for a customer.
- `GET /customer/{customer_id}/invoice`: Retrieve all invoices for a specific customer.
- `GET /invoice/{invoice_no}`: Fetch details of a specific invoice.
- `GET /invoice/{invoice_no}/{stockcode}/`: Fetch a specific stock code on the invoice.
- `POST /invoice/{invoice_no}/{stockcode}/`: Add a stock code to the invoice.

## Built With

- [FastAPI](https://fastapi.tiangolo.com/) - Modern, fast web framework for building APIs with Python 3.7+.
- [Docker](https://www.docker.com/) - Containerization and deployment.


