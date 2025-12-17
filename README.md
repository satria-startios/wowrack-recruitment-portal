# WowRack Recruitment Portal

A modern recruitment portal designed to streamline the hiring process for WowRack. This application provides an intuitive interface for managing job postings, applicant tracking, and recruitment workflows.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Setup Instructions](#setup-instructions)
- [Configuration](#configuration)
- [Running the Application](#running-the-application)
- [Development](#development)
- [Contributing](#contributing)
- [License](#license)

## Project Overview

The WowRack Recruitment Portal is a comprehensive solution for managing the entire recruitment lifecycle. It enables:

- **Job Management**: Create, edit, and manage job postings
- **Application Tracking**: Track applicants through different stages of the hiring process
- **Candidate Management**: Maintain detailed candidate profiles and evaluation records
- **Workflow Automation**: Automate recruitment workflows and notifications
- **Reporting & Analytics**: Generate insights on recruitment metrics and performance

## Features

- ✅ User-friendly job posting interface
- ✅ Applicant tracking system (ATS)
- ✅ Candidate profile management
- ✅ Interview scheduling
- ✅ Email notifications
- ✅ Dashboard and analytics
- ✅ Role-based access control
- ✅ Mobile-responsive design

## Prerequisites

Before you begin, ensure you have the following installed:

- **Node.js** (v16.0.0 or higher)
- **npm** (v8.0.0 or higher) or **yarn** (v1.22.0 or higher)
- **Git** (v2.25.0 or higher)
- **Database**: PostgreSQL 12+ or MySQL 8.0+ (depending on configuration)
- **Environment Variables**: Properly configured .env file

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/satria-startios/wowrack-recruitment-portal.git
cd wowrack-recruitment-portal
```

### 2. Install Dependencies

Using npm:
```bash
npm install
```

Or using yarn:
```bash
yarn install
```

### 3. Set Up Environment Variables

Create a `.env` file in the root directory and add the following variables:

```env
# Server Configuration
NODE_ENV=development
PORT=3000
APP_URL=http://localhost:3000

# Database Configuration
DB_HOST=localhost
DB_PORT=5432
DB_NAME=wowrack_recruitment
DB_USER=your_db_user
DB_PASSWORD=your_db_password

# Authentication
JWT_SECRET=your_jwt_secret_key_here
JWT_EXPIRE=7d

# Email Configuration
SMTP_HOST=smtp.gmail.com
SMTP_PORT=587
SMTP_USER=your_email@gmail.com
SMTP_PASSWORD=your_app_password
SMTP_FROM=noreply@wowrack.com

# AWS Configuration (Optional)
AWS_ACCESS_KEY_ID=your_aws_key
AWS_SECRET_ACCESS_KEY=your_aws_secret
AWS_REGION=us-east-1

# API Keys
RECAPTCHA_SITE_KEY=your_recaptcha_key
RECAPTCHA_SECRET_KEY=your_recaptcha_secret
```

## Setup Instructions

### Step 1: Database Setup

Create the database and run migrations:

```bash
npm run db:create
npm run db:migrate
npm run db:seed  # (Optional) Seed sample data
```

### Step 2: Install Dependencies

```bash
npm install
```

### Step 3: Configure Environment Variables

Update the `.env` file with your actual configuration values.

### Step 4: Build the Application (if applicable)

```bash
npm run build
```

### Step 5: Verify Installation

Run tests to ensure everything is set up correctly:

```bash
npm run test
```

## Configuration

### Database Configuration

Update `src/config/database.js` or set the environment variables as described in the `.env` file.

### Email Configuration

Configure your SMTP settings in the `.env` file for email notifications to work properly.

### Authentication

JWT tokens are used for authentication. Ensure the `JWT_SECRET` is set to a strong, random value in production.

## Running the Application

### Development Mode

```bash
npm run dev
```

The application will be available at `http://localhost:3000`

### Production Mode

```bash
npm run build
npm start
```

### Using Docker (Optional)

If Docker is configured:

```bash
docker build -t wowrack-recruitment .
docker run -p 3000:3000 --env-file .env wowrack-recruitment
```

## Development

### Project Structure

```
wowrack-recruitment-portal/
├── src/
│   ├── components/       # React components
│   ├── pages/           # Page components
│   ├── services/        # API services
│   ├── utils/           # Utility functions
│   ├── config/          # Configuration files
│   └── styles/          # CSS/SCSS files
├── public/              # Static files
├── tests/               # Test files
├── .env.example         # Example environment file
├── package.json         # Project dependencies
└── README.md           # This file
```

### Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm start` - Start production server
- `npm test` - Run test suite
- `npm run lint` - Run code linter
- `npm run format` - Format code with Prettier

### Code Style

This project follows ESLint and Prettier configurations. Run `npm run format` before committing changes.

## Contributing

We welcome contributions! Please follow these guidelines:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

Please ensure:
- Your code follows the project's code style
- Tests are written for new features
- The test suite passes (`npm test`)
- Documentation is updated accordingly

## Troubleshooting

### Common Issues

**Issue**: Database connection error
- **Solution**: Verify your database credentials in `.env` file and ensure the database server is running.

**Issue**: Port 3000 is already in use
- **Solution**: Change the `PORT` environment variable or kill the process using port 3000.

**Issue**: Email not sending
- **Solution**: Check SMTP configuration and ensure "Less secure app access" is enabled for Gmail accounts.

### Getting Help

For issues and questions:
- Check the [Issues](https://github.com/satria-startios/wowrack-recruitment-portal/issues) page
- Review existing documentation
- Contact the development team

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Last Updated**: 2025-12-17

For more information, visit the [GitHub Repository](https://github.com/satria-startios/wowrack-recruitment-portal)
