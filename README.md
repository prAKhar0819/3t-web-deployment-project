Project Title: Three-tier Application Deployment on AWS EKS

Overview:
This project involves deploying a cloud-native, three-tier application using AWS EKS. The application architecture comprises three main components:

1. Frontend (React): The presentation layer is developed using React, containerized with Docker, and deployed as a service in the EKS cluster.


2. Backend (Node.js): The application logic is handled by a Node.js service, containerized with Docker, and managed within the EKS cluster.


3. Database (MongoDB): The data layer uses MongoDB, also containerized and deployed within the Kubernetes cluster to maintain data persistence and reliability.



Architecture Breakdown:

Containerization: Each component (React, Node.js, and MongoDB) is independently containerized using Docker to provide a consistent and portable runtime environment across development, testing, and production stages.

Kubernetes Orchestration: Kubernetes orchestrates and manages the application deployment within AWS EKS, ensuring scalability, load balancing, and high availability.

AWS EKS: The application is hosted on AWS Elastic Kubernetes Service (EKS), which provides a managed Kubernetes environment for scalable and secure deployment.

AWS Load Balancer and Ingress Controller: AWS Load Balancer Controller and Kubernetes Ingress are utilized for efficient traffic distribution. The Ingress controller routes external HTTP/S traffic to the services, ensuring secure and seamless connectivity across the application components.

Service Discovery and Networking: Kubernetes services and networking configurations ensure internal and external communication between the frontend, backend, and database layers, supporting efficient data flow and service interaction.


Deployment Process:

1. IAM Configuration: An IAM user with AdministratorAccess is created for managing AWS services, and AWS CLI is configured with access credentials.


2. EKS Cluster Setup: Using eksctl, an EKS cluster is set up with two t2.medium nodes. Kubernetes CLI (kubectl) is configured for cluster management.


3. Application Deployment: Docker images for each component (React, Node.js, MongoDB) are built and deployed in the EKS cluster using Kubernetes manifests. The Ingress controller is configured to manage traffic routing and secure connections.


4. Load Balancer and Ingress Configuration: The AWS Load Balancer Controller is set up using Helm charts, and Kubernetes Ingress rules are defined for routing and managing traffic across the application services.



Key Technologies and Tools:

Docker: For containerizing application components.

AWS EKS and Kubernetes: For orchestrating and managing the deployment.

Kubernetes Ingress Controller: For managing HTTP/S routing and service access.

Helm: For managing the AWS Load Balancer Controller deployment.

AWS CLI and eksctl: For AWS resource configuration and EKS cluster management.
