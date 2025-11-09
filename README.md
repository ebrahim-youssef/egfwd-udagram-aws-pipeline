# Udagram Full Stack Application

## CircleCI Build Status:

Click To See The Latest Builds ↓

[![Ibrahim-Rezq](https://circleci.com/gh/Ibrahim-Rezq/udagram-full-stack.svg?style=svg)](https://app.circleci.com/pipelines/github/Ibrahim-Rezq/udagram-full-stack?branch=main&filter=all)

![Website Screenshot](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/Website.png)

---

## 📋 Project Overview

A full-stack web application built with **Angular** frontend and **Node.js/Express** backend. The application was provided as part of the Udacity Full Stack Nanodegree Program. This project showcases my work in implementing **CI/CD pipelines**, **AWS infrastructure setup**, and **DevOps practices** including automated deployment, cloud service configuration, and continuous integration with CircleCI.

---

## 🏗️ Architecture & Infrastructure

### AWS RDS (Relational Database Service)
PostgreSQL database hosting for reliable and scalable data storage.

![RDS Screenshot](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/RDS.png)

### AWS Elastic Beanstalk
Automated deployment and scaling for the Node.js backend API.

![Elastic Beanstalk Screenshot](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/EB_ENV.png)

### AWS S3 Bucket
Static website hosting for the Angular frontend application.

![S3 Bucket Screenshot](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/S3_bucket.png)

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v14 or higher)
- npm (v6 or higher)
- AWS CLI configured
- Angular CLI v12.2.16

### Installation

Install dependencies for both frontend and backend:

```bash
# Install frontend dependencies
npm run front-end-install

# Install backend dependencies
npm run back-end-install
```

### Available Scripts

#### Frontend Commands
```bash
npm run front-end-install   # Install Angular dependencies
npm run front-end-test      # Run frontend tests
npm run front-end-lint      # Lint frontend code
npm run front-end-build     # Build Angular app for production
npm run front-end-deploy    # Deploy frontend to AWS S3
```

#### Backend Commands
```bash
npm run back-end-install    # Install Node.js dependencies
npm run back-end-build      # Build backend TypeScript code
npm run back-end-deploy     # Deploy backend to AWS Elastic Beanstalk
npm run setEnv              # Set environment variables
```

---

## 📊 CI/CD Pipeline

### Pipeline Process Diagram

The application uses **CircleCI** for continuous integration and deployment, automatically building and deploying both frontend and backend on every commit to the main branch.

![Pipeline Diagram](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/Pipeline_Diagram.png)

### Deployment Flow:
1. **Code Push** → GitHub Repository
2. **CircleCI Trigger** → Automated build process
3. **Frontend Build** → Angular compilation
4. **Backend Build** → TypeScript compilation
5. **Deployment** → AWS S3 (Frontend) & Elastic Beanstalk (Backend)

---

## 🏛️ Infrastructure Architecture

### System Diagram

![Infrastructure Diagram](https://github.com/Ibrahim-Rezq/udagram-full-stack/blob/main/Documentation/Screenshots/Udagram_Diagram.png)

### Components:
- **Frontend**: Angular SPA hosted on S3
- **Backend**: Express REST API on Elastic Beanstalk
- **Database**: PostgreSQL on RDS
- **CI/CD**: CircleCI automation
- **Storage**: S3 for static assets

---

## 🛠️ Technology Stack

### Frontend
- Angular v12
- TypeScript
- HTML5/CSS3

### Backend
- Node.js
- Express
- TypeScript

### Cloud & DevOps
- AWS S3
- AWS Elastic Beanstalk
- AWS RDS (PostgreSQL)
- CircleCI

---

## 📁 Project Structure

```
udagram-full-stack/
├── udagram-frontend/     # Angular frontend application
├── udagram-api/          # Node.js/Express backend API
├── Documentation/        # Project documentation & screenshots
└── package.json          # Root package with deployment scripts
```

---

## 🔐 Environment Variables

Backend environment variables need to be set using:
```bash
npm run setEnv
```

Required variables include database credentials, AWS configuration, and API keys.

---

## 📝 Project Context

The base application was provided by **Udacity** as part of the Full Stack Nanodegree Program. 

**My Contributions:**
- Complete CI/CD pipeline implementation with CircleCI
- AWS infrastructure setup and configuration (RDS, Elastic Beanstalk, S3)
- Automated deployment workflows for both frontend and backend
- Environment configuration and management
- DevOps best practices implementation
- Project documentation and architecture diagrams

---

## 👤 Author

**Ibrahim Rezq**

- GitHub: [@Ibrahim-Rezq](https://github.com/Ibrahim-Rezq)
- Repository: [udagram-full-stack](https://github.com/Ibrahim-Rezq/udagram-full-stack)

**Role:** DevOps Engineer & CI/CD Implementation

---

## 🙏 Acknowledgments

- Udacity Full Stack Nanodegree Program for providing the base application
- AWS Documentation
- CircleCI Documentation
