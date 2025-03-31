# WeLocal Local Services Service

Community services management service for the WeLocal platform, built with Node.js and Express.

## Tech Stack

- **Runtime**: Node.js
- **Framework**: Express.js
- **Database**: PostgreSQL
- **Authentication**: JWT (JSON Web Tokens)
- **API Documentation**: Swagger/OpenAPI
- **Testing**: Jest
- **Logging**: Winston
- **Validation**: Joi
- **ORM**: TypeORM
- **File Storage**: AWS S3
- **Search Engine**: Elasticsearch
- **Payment Processing**: Stripe
- **Email Service**: SendGrid
- **SMS Service**: Twilio
- **Real-time Communication**: Socket.io

## Features

- Service provider profiles
- Service request management
- Service scheduling
- Emergency services
- Service categories
- Provider ratings and reviews
- Service pricing
- Service area mapping
- Service availability tracking
- Service provider verification
- Community feedback
- Service analytics

## Prerequisites

- Node.js (v18 or higher)
- PostgreSQL
- Elasticsearch
- npm or yarn
- AWS S3 bucket
- Stripe account
- SendGrid account
- Twilio account
- Redis (for real-time features)

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-org/welocal-local-services-service.git
   cd welocal-local-services-service
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   ```

3. Create environment file:
   ```bash
   cp .env.example .env
   ```

4. Configure environment variables in `.env`:
   ```env
   NODE_ENV=development
   PORT=8086
   DATABASE_URL=postgresql://welocal:welocal123@localhost:5432/welocal
   ELASTICSEARCH_URL=http://localhost:9200
   AWS_ACCESS_KEY_ID=your-aws-access-key
   AWS_SECRET_ACCESS_KEY=your-aws-secret-key
   AWS_REGION=your-aws-region
   AWS_S3_BUCKET=your-s3-bucket
   STRIPE_SECRET_KEY=your-stripe-secret-key
   SENDGRID_API_KEY=your-sendgrid-api-key
   TWILIO_ACCOUNT_SID=your-twilio-account-sid
   TWILIO_AUTH_TOKEN=your-twilio-auth-token
   REDIS_URL=redis://localhost:6379
   ```

## Running the Service

### Development Mode
```bash
npm run dev
# or
yarn dev
```

### Production Mode
```bash
npm run build
npm start
# or
yarn build
yarn start
```

### Docker
```bash
docker build -t welocal-local-services-service .
docker run -p 8086:8086 welocal-local-services-service
```

## API Endpoints

### Service Providers
- `GET /api/v1/providers` - Get service providers list
- `POST /api/v1/providers` - Create provider profile
- `GET /api/v1/providers/:id` - Get provider details
- `PUT /api/v1/providers/:id` - Update provider profile
- `DELETE /api/v1/providers/:id` - Delete provider profile

### Service Categories
- `GET /api/v1/categories` - Get service categories
- `POST /api/v1/categories` - Create category
- `GET /api/v1/categories/:id` - Get category details
- `PUT /api/v1/categories/:id` - Update category
- `DELETE /api/v1/categories/:id` - Delete category

### Service Requests
- `GET /api/v1/requests` - Get service requests
- `POST /api/v1/requests` - Create service request
- `GET /api/v1/requests/:id` - Get request details
- `PUT /api/v1/requests/:id/status` - Update request status
- `DELETE /api/v1/requests/:id` - Cancel request

### Emergency Services
- `POST /api/v1/emergency` - Create emergency request
- `GET /api/v1/emergency/:id` - Get emergency request details
- `PUT /api/v1/emergency/:id/status` - Update emergency status
- `GET /api/v1/emergency/nearby` - Get nearby emergency services

### Reviews and Ratings
- `GET /api/v1/providers/:id/reviews` - Get provider reviews
- `POST /api/v1/reviews` - Create review
- `PUT /api/v1/reviews/:id` - Update review
- `DELETE /api/v1/reviews/:id` - Delete review

## API Documentation

API documentation is available at `/api-docs` when running the service.

## Testing

### Unit Tests
```bash
npm run test
# or
yarn test
```

### Integration Tests
```bash
npm run test:integration
# or
yarn test:integration
```

### E2E Tests
```bash
npm run test:e2e
# or
yarn test:e2e
```

## Project Structure

```
src/
├── config/           # Configuration files
├── controllers/      # Route controllers
├── middleware/       # Custom middleware
├── models/          # Database models
├── routes/          # API routes
├── services/        # Business logic
├── utils/           # Utility functions
├── validators/      # Request validation
├── storage/         # File storage handling
├── search/          # Search functionality
├── payments/        # Payment processing
├── notifications/   # Email and SMS notifications
├── emergency/       # Emergency services handling
└── app.js           # Application entry point
```

## Security Features

- JWT token-based authentication
- Rate limiting
- CORS configuration
- Helmet security headers
- Input validation
- SQL injection prevention
- XSS protection
- File upload validation
- Secure payment processing
- Emergency service verification

## Monitoring

The service exposes the following endpoints for monitoring:
- `/health` - Health check
- `/metrics` - Prometheus metrics
- `/status` - Service status

## Logging

Logs are written to:
- Console (development)
- File (production)

Log levels:
- ERROR
- WARN
- INFO
- DEBUG

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Your License Here]

## Support

For support, please contact [Your Contact Information] 