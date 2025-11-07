<!-- # Database Design

The system uses **PostgreSQL** as the primary relational database to store user, project, and deployment information.  
It serves as the backbone for authentication, build tracking, and deployment management.

## Overview

The database consists of three main entities:

### 1. User Table
- Stores user authentication and profile details.  
- Each user can create and manage multiple projects.  
- Used for login verification and access control.

### 2. Project Table
- Represents an application or repository that the user wants to deploy.  
- Stores information such as the project name, repository source, and associated user.  
- Each project can have multiple deployments over time.

### 3. Deployment Table
- Tracks every build and deployment attempt for a project.  
- Includes information such as build status, logs, timestamps, and output location (e.g., S3 path).  
- Each deployment entry is linked to a specific project.

## Relationships

- A **User** can have multiple **Projects**.  
- Each **Project** can have multiple **Deployments**.  
- This one-to-many relationship enables users to manage multiple apps, each with versioned deployments.

## Purpose

This design ensures:
- Clear separation of user data, project metadata, and deployment history.  
- Scalable and efficient tracking of application lifecycle.  
- Simplified retrieval of deployment status and history for each user or project. -->
