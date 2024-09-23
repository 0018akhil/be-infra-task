## One

# Project Setup Instructions

This document provides instructions for setting up the project on your local machine.

## Prerequisites

Make sure you have the following installed:

- Docker
- Docker Compose

## Project Structure

The project consists of several microservices, including:

- PostgreSQL database
- API services:
  - Orders
  - Products
  - Users
- Nginx as a reverse proxy

## Environment Variables

Create a `.env` file in the root of your project directory with the following content:

```plaintext
DB_HOST='postgres'
DB_USERNAME='user'
DB_PASSWORD='password'
DB_DATABASE='mydatabase'
```

## Docker Compose Setup

### Clone the Repository

Clone the project repository to your local machine:

```bash
git clone <repository-url>
cd <repository-directory>
```

### Build and Run the Containers

Run the following command to build and start the Docker containers:

```bash
docker-compose up --build
```

This will start the PostgreSQL database and the API services, along with Nginx.

### Access the APIs

You can access the APIs through Nginx at the following endpoints:

- Orders: [http://localhost/orders](http://localhost/orders)
- Products: [http://localhost/products](http://localhost/products)
- Users: [http://localhost/users](http://localhost/users)

### Stopping the Containers

To stop the running containers, use:

```bash
docker-compose down
```

## Notes

- Ensure that your Docker daemon is running before executing the commands.
- If you make changes to the code, you may need to rebuild the containers using the `--build` flag.

## Troubleshooting

If you encounter any issues, make sure to check the logs of the respective containers for more information:

```bash
docker-compose logs <service-name>
```

Replace `<service-name>` with the name of the service you want to inspect (e.g., `api1`, `api2`, `api3`, `postgres`, or `nginx`).

Feel free to replace `<repository-url>` and `<repository-directory>` with your actual repository URL and directory name. Let me know if you need any modifications!
