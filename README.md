# Rayagate Challenge

This project is a full-stack application built with a Laravel API, a Nuxt.js frontend, and an Nginx reverse proxy. It is containerized using Docker for easy deployment and scalability.

## Project Structure

- **API**: A Laravel backend that provides a REST API.
- **Client**: A Nuxt.js frontend that communicates with the Laravel API.
- **Nginx**: A reverse proxy that handles routing requests to the appropriate services (API or Client).

## Requirements

- Docker
- Docker Compose

## Setup

### Clone the Repository

Clone the repository to your local machine:

```bash
git clone <repository-url>
cd <repository-folder>
```

### Configure SSL Certificates

Ensure you have valid SSL certificates. The `nginx/certs/` folder should contain the following files:

- `self.crt`: Your SSL certificate.
- `self.key`: Your SSL private key.

For development, you can generate self-signed certificates.

### Environment Configuration

Make sure to configure the environment variables for your Laravel API and MySQL database in the `docker-compose.yml` file under the `api` service. The default values should be suitable for a local development environment.

### Build and Start the Containers

Run the following command to build and start all services (API, Client, MySQL, Nginx):

```bash
docker-compose up --build
```

## Accessing the Application

### Frontend (Nuxt.js)

Once the containers are up, you can access the Nuxt.js application in your browser at: https://localhost:3000

**Screenshot Example**:  
![Nuxt.js Frontend](C:/Users/Omar/Desktop/rayagate_challenge/httpslocalhost3000.jpeg)

### API (Laravel)

The API is available at: https://localhost:8000

**Screenshot Example**:  
![Laravel API](C:/Users/Omar/Desktop/rayagate_challenge/httpslocalhost8000.jpeg)
```