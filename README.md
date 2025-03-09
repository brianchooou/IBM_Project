# Task Management API

A RESTful API service built with Node.js, Express, and MongoDB for managing tasks. This service is containerized using Podman/Docker.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 🚀 Features

- RESTful API endpoints for CRUD operations
- Swagger/OpenAPI documentation
- Containerized deployment (Podman/Docker)
- Logging system (Winston)
- Environment-based configuration
- MongoDB database integration

## 📋 Prerequisites

- Node.js (v14 or higher)
- Podman/Docker
- Podman Compose/Docker Compose
- MongoDB (containerized or local instance)

## 🛠 Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB
- **Documentation**: Swagger/OpenAPI
- **Logging**: Winston
- **Containerization**: Podman/Docker
- **API Testing**: Postman, Jest

## 🔧 Installation & Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/brianchooou/IBM_Project.git
   cd api-demo
   ```

2. **Environment Setup**
   ```bash
   # Copy example environment file
   cp .env.example .env
   
   # Edit .env file with your configurations
   # Required variables:
   # - PORT=3000
   # - MONGODB_URI=mongodb://admin:password@mongodb:27017/taskdb?authSource=admin
   # - NODE_ENV=development
   ```

3. **Using Podman/Docker Compose**
   ```bash
   # Start the services
   podman-compose up -d
   
   # Check service status
   podman-compose ps
   ```

## 📚 API Documentation

Once the service is running, access the Swagger documentation at:
```
http://localhost:3000/api-docs
```

### API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | /api/tasks | Get all tasks |
| GET | /api/tasks/:id | Get a specific task |
| POST | /api/tasks | Create a new task |
| PUT | /api/tasks/:id | Update a task |
| DELETE | /api/tasks/:id | Delete a task |

## 🔍 Monitoring & Observability

- **Logging**
  - Error logs: `logs/error.log`
  - Combined logs: `logs/combined.log`
  - Console output in development mode

## 🧪 Testing

```bash
# Run tests
npm test

# Run tests with coverage
npm run test:coverage
```

## 🔒 Security

- CORS protection enabled
- Environment variable management
- Container network isolation
- Error handling middleware

## 🚀 Deployment

### Production Deployment Steps

1. Set environment variables for production
2. Build and push Docker images
3. Deploy using container orchestration
4. Monitor logs and performance

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👥 Authors

- **Brian Chou** - *Initial work*

## 🙏 Acknowledgments

- Node.js community
- Express.js framework
- MongoDB team
- Docker/Podman community 