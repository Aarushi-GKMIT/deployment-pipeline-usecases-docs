<!-- # System Architecture

## Components

| Component | Technology | Description |
|------------|-------------|-------------|
| **Frontend** | React.js | User interface for login, project creation, deployment trigger |
| **API Server** | Express/Flask | Handles authentication, manages projects, triggers builds |
| **Build Servers** | AWS ECS + Docker | Run build containers using images from AWS ECR |
| **Storage** | AWS S3 | Stores compiled build files |
| **Reverse Proxy** | Node.js | Serves S3 content as hosted URLs |
| **Database** | PostgreSQL | Stores user, project, and deployment records |

**Flow:**
1. User logs in → submits GitHub repo URL.  
2. API server triggers ECS build.  
3. ECS container builds and uploads files to S3.  
4. Reverse proxy serves deployed app from S3.  
5. Database tracks each deployment. -->
