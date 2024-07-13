# TODO APP API 

# Technical Design Document

## 1. Introduction

### Purpose
The purpose of this document is to provide a comprehensive technical design for the TODO App API. It details the architecture, components, data design, and implementation strategies necessary to develop and deploy the API.

### Scope
This document covers the design and development of the TODO App API backend, database schema, authentication mechanisms, third-party integrations, security considerations, testing strategies, deployment plan, and maintenance guidelines.

### Definitions, Acronyms, and Abbreviations
- **API**: Application Programming Interface
- **JWT**: JSON Web Token
- **ER**: Entity-Relationship
- **GDPR**: General Data Protection Regulation
- **AWS**: Amazon Web Services
- **Node.js**: JavaScript runtime built on Chrome's V8 JavaScript engine
- **PostgreSQL**: Open-source relational database management system

## 2. System Overview

### System Description
The TODO App API is a backend service that provides endpoints for managing tasks. It allows users to create, read, update, and delete tasks. The API uses JWT for authentication and integrates with an email service for notifications.

### Goals and Objectives
- Provide a reliable and scalable API for managing tasks.
- Ensure secure access through JWT authentication.
- Comply with GDPR for data protection.
- Integrate seamlessly with third-party email services.
- Deliver high performance and efficient response times.

## 3. Architecture Design

### System Architecture
The system architecture consists of a RESTful API built with Node.js and Express.js, a PostgreSQL database for data storage, JWT for authentication, and integration with an email service for notifications.

### Component Diagram
![Component Diagram](https://eraser.imgix.net/workspaces/tufSxadkRBIVVXLNnZDZ/cgftjyxbLVNyDnzTOdHDVn4r5S43/yXLO_X9EtFAG1rMtNUn1T.png?ixlib=js-3.7.0)

## 4. Detailed Design

### 4.1 Backend

#### Programming Language
JavaScript (Node.js)

#### Framework
Express.js

#### API Endpoints
- **/api/todos**
    - **GET**: Get All Tasks
    - **POST**: Create a Task
- **/api/todos/{taskId}**
    - **GET**: Get Task by ID
    - **PUT**: Update Task
    - **DELETE**: Delete Task

### 4.2 Database

#### Database Technology
PostgreSQL

#### Schema Design
The database schema includes tables for tasks, users, and any other necessary entities.

#### ER Diagram
![ER Diagram](https://eraser.imgix.net/workspaces/tufSxadkRBIVVXLNnZDZ/cgftjyxbLVNyDnzTOdHDVn4r5S43/2aZLTYTRoSYRV5xe5C3Hb.png?ixlib=js-3.7.0)

### 4.3 Authentication

#### Authentication Method
JWT (JSON Web Token)

#### Flow Diagram
![Authentication Flow Diagram](https://eraser.imgix.net/workspaces/tufSxadkRBIVVXLNnZDZ/cgftjyxbLVNyDnzTOdHDVn4r5S43/DyhLt8qaxQZcZzQ5T7Nuc.png?ixlib=js-3.7.0)

### 4.4 Third-Party Services

#### Email Service
The system integrates with an email service to send notifications to users. The integration details include API endpoints and authentication methods required to interact with the email service.

## 5. Data Design

### Data Models
- **Task**
    - id: string
    - title: string
    - description: string
    - completed: boolean
- **TaskCreate**
    - title: string
    - description: string
- **TaskUpdate**
    - title: string
    - description: string
    - completed: boolean

## 6. Security Considerations

### Compliance Standards
GDPR

### Security Measures
- Use of HTTPS for secure communication.
- Implementation of JWT for secure authentication.
- Regular security audits and vulnerability assessments.

## 7. Performance Metrics

### Performance Requirements
- API response time should be under 200ms.
- The system should handle up to 1000 concurrent users.
- Database queries should be optimized for quick retrieval.

## 8. Testing Strategy

### Unit Testing
Unit tests will be written for individual functions and components to ensure they work as expected.

### Integration Testing
Integration tests will be conducted to ensure that different parts of the system work together seamlessly.

### End-to-End Testing
End-to-end tests will simulate real user scenarios to ensure the entire system functions correctly from start to finish.

## 9. Deployment Plan

### Deployment Environment
AWS

### Deployment Steps
1. Set up AWS infrastructure.
2. Configure the environment and deploy the backend services.
3. Set up the PostgreSQL database.
4. Deploy the application and run initial tests.
5. Monitor and maintain the system.

## 10. Maintenance and Support

### Maintenance Plan
Regular updates and patches will be applied to ensure the system remains secure and efficient. Performance monitoring tools will be used to identify and address any issues.

### Support Resources
- Documentation
- User support portal
- Regular updates and bug fixes

## 11. Appendices

### Glossary
- **API**: Application Programming Interface
- **JWT**: JSON Web Token
- **ER**: Entity-Relationship
- **GDPR**: General Data Protection Regulation
- **AWS**: Amazon Web Services
- **Node.js**: JavaScript runtime built on Chrome's V8 JavaScript engine
- **PostgreSQL**: Open-source relational database management system

### References
- Project GitHub Repository: [link](https://github.com/cruso003/hng_boilerplate_node_web)
- Swagger API Documentation: [Link](https://app.swaggerhub.com/apis/HADM/TODOAPI/1) 
- Node.js Documentation: []
- PostgreSQL Documentation: []
