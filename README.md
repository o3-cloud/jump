# Jump URL Shortening Service

Jump is a URL shortening service that allows users to shorten long URLs into more manageable and memorable short URLs. This project provides a robust API for URL shortening, user authentication, analytics, and custom short URLs. The GUI development is deferred to a later stage.

## Table of Contents

- [Features](#features)
- [Technology Stack](#technology-stack)
- [Setup and Installation](#setup-and-installation)
- [API Documentation](#api-documentation)
- [Development](#development)
- [Testing](#testing)
- [Deployment](#deployment)
- [Monitoring and Logging](#monitoring-and-logging)
- [Contributing](#contributing)
- [License](#license)

## Features

- **URL Shortening**: Shorten long URLs into short, easy-to-remember URLs.
- **User Authentication**: Integration with GitHub for federated identity authentication.
- **Analytics**: Track general KPIs such as the number of URLs shortened and user engagement.
- **Custom Short URLs**: Allow users to create custom short URLs.

## Technology Stack

- **Backend**: TypeScript with NestJS framework
- **Database**: PostgreSQL
- **Frontend**: React (deferred)
- **CI/CD**: GitHub Actions
- **Deployment**: Kubernetes cluster
- **Local Development**: Docker
- **Monitoring and Logging**: Grafana and Prometheus (to be integrated towards the end)

## Setup and Installation

### Prerequisites

- Node.js
- Docker
- Kubernetes cluster
- GitHub account for authentication

### Clone the Repository

```bash
git clone https://github.com/yourusername/jump.git
cd jump
```

### Install Dependencies

```bash
npm install
```

### Environment Variables

Create a `.env` file in the root directory and add the following environment variables:

```env
DATABASE_URL=postgres://username:password@localhost:5432/jump
GITHUB_CLIENT_ID=your_github_client_id
GITHUB_CLIENT_SECRET=your_github_client_secret
JWT_SECRET=your_jwt_secret
```

### Run the Application

```bash
npm run start:dev
```

## API Documentation

The API schema is defined using OpenAPI specifications. You can view the API documentation by running the application and navigating to `http://localhost:3000/api`.

## Development

### Initial Setup

Set up the development environment, including NestJS, PostgreSQL, and Docker.

### Define API Schema

Use OpenAPI specifications to define the API schema for URL shortening, user authentication, analytics, and custom short URLs.

### API Development with TDD

Write tests for the core API functionalities based on the OpenAPI specs before implementing them.

### CI/CD Pipeline

Set up GitHub Actions for CI/CD to automate testing and deployment processes.

## Testing

We follow Test Driven Development (TDD) methodology. To run the tests, use the following command:

```bash
npm run test
```

## Deployment

### Build Docker Image

```bash
docker build -t jump-url-shortener .
```

### Deploy to Kubernetes

Ensure your Kubernetes cluster is set up and configured. Then deploy the application using the following command:

```bash
kubectl apply -f k8s/deployment.yaml
```

## Monitoring and Logging

Integrate Grafana and Prometheus for monitoring and logging. This will be done towards the end of the project.

## Contributing

We welcome contributions! Please follow these steps to contribute:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Create a new Pull Request.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.