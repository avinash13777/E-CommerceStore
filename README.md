# E-CommerceStore – End-to-End DevOps Deployment

## 1. Project Overview

**E-CommerceStore** is a MERN-based e-commerce application consisting of a React frontend and multiple Node.js backend microservices.

The project demonstrates how to containerize the application, store Docker images in AWS ECR, provision AWS infrastructure using Terraform, and deploy the application to Amazon EKS using Kubernetes.

### Project Flow

```text
Developer Code
      ↓
   GitHub
      ↓
 Docker Images
      ↓
    AWS ECR
      ↓
 Terraform
      ↓
    AWS EKS
      ↓
 Kubernetes Deployments
      ↓
 E-Commerce Application
```

---

# 2. Technologies Used

### Application

* React.js
* Node.js
* Express.js
* MongoDB
* REST APIs

### DevOps

* Git & GitHub
* Docker
* AWS ECR
* Terraform
* Kubernetes
* Amazon EKS
* AWS CLI
* kubectl

### AWS Services

* Amazon EKS
* Amazon ECR
* Amazon VPC
* EC2 / EKS Managed Node Group
* Elastic Load Balancer
* CloudWatch Logs

---

# 3. Project Structure

```text
E-CommerceStore/
│
├── backend/
│   │
│   ├── user-service/
│   │   ├── Dockerfile
│   │   ├── models/
│   │   ├── routes/
│   │   ├── middleware/
│   │   ├── package.json
│   │   └── server.js
│   │
│   ├── product-service/
│   │   ├── Dockerfile
│   │   ├── models/
│   │   ├── routes/
│   │   ├── package.json
│   │   └── server.js
│   │
│   ├── cart-service/
│   │   ├── Dockerfile
│   │   ├── models/
│   │   ├── routes/
│   │   ├── package.json
│   │   └── server.js
│   │
│   └── order-service/
│       ├── Dockerfile
│       ├── models/
│       ├── routes/
│       ├── package.json
│       └── server.js
│
├── frontend/
│   ├── Dockerfile
│   ├── public/
│   ├── src/
│   │   ├── components/
│   │   ├── contexts/
│   │   ├── pages/
│   │   └── services/
│   └── package.json
│
├── kubernetes/
│   ├── user.yaml
│   ├── product.yaml
│   ├── cart.yaml
│   ├── order.yaml
│   └── frontend.yaml
│
├── terraform/
│   └── main.tf
│
├── .gitignore
├── LICENSE
└── README.md
```

---

# 4. Application Architecture

The application is divided into five services.

| Service         | Port | Purpose                              |
| --------------- | ---: | ------------------------------------ |
| Frontend        | 3000 | React user interface                 |
| User Service    | 3001 | User registration and authentication |
| Product Service | 3002 | Product and category management      |
| Cart Service    | 3003 | Shopping cart management             |
| Order Service   | 3004 | Orders and payments                  |

The backend services are designed as independent microservices.

---

# 5. Step 1 – Clone the Repository

```bash
git clone https://github.com/avinash13777/E-CommerceStore.git
cd E-CommerceStore
```

---

# 6. Step 2 – Verify the Application

Check the project structure:

```bash
ls
```

Expected directories:

```text
backend
frontend
terraform
kubernetes
```

---

# 7. Step 3 – Dockerize the Appli
