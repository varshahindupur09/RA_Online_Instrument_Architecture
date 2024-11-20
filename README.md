# RA_Online_Instrument_Architecture
This repository is created to explain the project architecture. 

![image](https://github.com/user-attachments/assets/9dded5ee-6590-4c74-9065-40d63824d442)


System Design for 10,000 Users (Initial Decision)
This architecture showcases a scalable and secure web application designed to handle 10,000 users. The survey sample size later increased to 2M+ users.

Key Components and AWS Services
Domain and DNS Management:

Service: Amazon Route 53
Purpose: Manages DNS resolution for routing user requests to the application’s frontend webpage.
Content Delivery and Security:

Service: Amazon CloudFront
Purpose: Provides caching at the edge, improves performance, ensures security, and delivers frontend content.
Frontend Hosting:

Service: Amazon S3
Purpose: Hosts the React.js-based static frontend, which is accessed through CloudFront for optimized delivery.
API Gateway:

Service: Amazon API Gateway
Purpose: Acts as the entry point for all API calls to the backend, ensuring secure and scalable communication.
Backend Hosting and Scaling:

Services:
AWS Elastic Beanstalk
EC2 Auto Scaling Group
Load Balancer
Purpose: Runs backend services built with Node.js (Express.js and Mongoose.js). Docker containers are deployed on EC2 instances for backend scalability.
Backend Development:

Frameworks:
Node.js
Express.js
Mongoose.js
Purpose: Handles API logic and business functionalities.
Database:

Service: MongoDB (Managed in the Cloud)
Purpose: Stores and manages the application’s data securely and efficiently.
Data Analysis and Research:

Tools: Data pipelines built for research and insights derived from user data for analysis and reporting.
Scalability Features
Auto Scaling Group: Dynamically adjusts EC2 instances based on traffic load.
Load Balancer: Ensures high availability and traffic distribution across backend instances.
CloudFront Caching: Reduces latency and ensures faster delivery of frontend assets.
Security
CloudFront Integration: Protects frontend access with enhanced security.
API Gateway: Secures API endpoints with authentication and throttling mechanisms.
This system design is built for scalability, ensuring a seamless experience for both initial and increased user bases.
