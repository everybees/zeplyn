# Crypto Address API

This service is designed to generate and manage cryptocurrency addresses using FastAPI and MongoDB. It offers a RESTful
API to create and retrieve addresses for supported cryptocurrencies. This service is part of a software wallet website
ensuring secure storage and recovery mechanisms for wallets.

## Features

- Generate cryptocurrency addresses for supported currencies (BTC, ETH).
- Retrieve a list of generated addresses.
- Secure storage for private keys and other sensitive information.
- Dockerized service ensuring easy deployment and scalability.

## Installation & Setup

### Prerequisites

- Docker and Docker Compose installed on your machine.

### Setup

1. Clone the Repository:

```sh
git clone https://github.com/everybees/zeplin
cd zeplin
```

2. Build and Run the Docker Containers:

```sh
docker-compose up --build
```

3. Access the API:
- Open your web browser or API client and navigate to:

```arduino
http://localhost:8000
```


## API Documentation

The API documentation is available at http://localhost:8000/docs


## Project Structure
```md
   /project_root
      /app
         /api
            __init__.py
            addresses.py # For address-related routes
            api.py # For including all the routers
         /core
            __init__.py
            config.py # Configuration settings
         /db
            __init__.py
            mongodb.py # MongoDB connection and helpers
         /models
            __init__.py
            addresses.py # Pydantic models for addresses
         /services
            __init__.py
            crypto_service.py # For Crypto-related operations
         /tests # For test cases
         main.py
         Dockerfile
         docker-compose.yml
         requirements.txt
```

## Running Tests

To run the tests, first find the container ID of your app container.
```sh
docker ps
```

You can exec into the running container:

```sh
docker exec -it <container_id> pytest /app/test_main.py
```

## To Do

- [ ] Add support for more cryptocurrencies.
- [ ] Add support for more wallets.
- [ ] Add support for HD Wallets.
- [ ] Add support for API authentication methods.
- [ ] Add support for API logging.
