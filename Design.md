# Software Design Description (SDD)

## 1. Introduction

### 1.1 Purpose
The purpose of this Software Design Description (SDD) is to provide a detailed design for the Flipkart clone e-commerce platform. This document describes the software's architecture, components, interfaces, and their interactions to ensure that the implementation meets the system's functional and non-functional requirements.

### 1.2 Scope
The Flipkart clone system is an e-commerce platform that enables users to browse, purchase, and pay for products online. Sellers can list and manage products on the platform, while administrators oversee operations. The system includes a mobile and web application, backend API services, payment processing, real-time notifications, and integration with services like courier systems and SMS gateways.

---

## 2. System Overview

### Key Features:
- **Customer Features**:
  - Browse products by category, brand, and price.
  - Add products to the cart and wishlist.
  - Secure checkout and payment options.
  - Track orders in real-time.
  - Product reviews and ratings.
  
- **Seller Features**:
  - Product listing and inventory management.
  - Order notifications and updates.
  - Earnings and performance dashboard.
  
- **Admin Features**:
  - Manage users (customers and sellers).
  - Product and category management.
  - Sales and system analytics.
  - Monitor transactions and disputes.

---

## 3. Architecture Design

### 3.1 Architecture Components

#### User Interfaces
- **Customer App/Web**
  - Registration/Login.
  - Product Search and Filters.
  - Shopping Cart and Wishlist.
  - Checkout and Payment Gateway.
  - Order History and Tracking.

- **Seller Dashboard**
  - Registration/Login with KYC Verification.
  - Product Management (Add, Edit, Remove).
  - Order Fulfillment Dashboard.
  - Sales Reports and Analytics.

- **Admin Dashboard**
  - User Management (Sellers and Customers).
  - Product Approval and Moderation.
  - Real-time Sales Monitoring.
  - Dispute and Return Management.

---

### 3.2 Backend Services

- **Authentication Service**: 
  Secure login and token-based user authentication (e.g., JWT).  

- **Product Catalog Service**: 
  Handles product listings, categories, and filters.  

- **Order Management Service**: 
  Tracks the lifecycle of orders from checkout to delivery.  

- **Payment Integration**: 
  Securely processes payments via gateways like Stripe, Razorpay, or PayPal.  

- **Notification Service**: 
  Real-time updates via email, SMS, and push notifications for order and delivery updates.

- **Recommendation Engine**: 
  Provides personalized product suggestions based on user behavior and preferences.

---

### 3.3 Databases

- **PostgreSQL**:
  Stores structured data such as user profiles, products, orders, and transactions.

- **Redis**:
  Caches frequently accessed data like product search results and user sessions.

- **ElasticSearch**:
  Powers the search functionality for fast and scalable product queries.

---

### 3.4 External APIs

- **Payment Gateway (Stripe/PayPal)**: 
  For secure payments, refunds, and settlements.

- **Courier API (Shiprocket/Delhivery)**: 
  For real-time order tracking and delivery status.

- **SMS Gateway (Twilio)**: 
  Sends SMS notifications for order updates and OTP verification.

- **Maps API (Google Maps)**: 
  For delivery address validation and logistics optimization.

---

### 3.5 Infrastructure

- **Hosting**: 
  Cloud services such as AWS or Google Cloud for backend, databases, and file storage.

- **Load Balancer**: 
  Nginx or AWS ELB for traffic distribution.

- **Monitoring Tools**: 
  Prometheus and Grafana for performance monitoring and logging.

- **CI/CD Pipeline**: 
  Automated builds and deployments using tools like GitHub Actions or Jenkins.

---

## 4. Module Design

### 4.1 Frontend Application

#### 4.1.1 User Interface (UI)
The UI is responsive and optimized for mobile and web:
- Home Page with featured products.
- Product Details Page.
- Cart and Checkout Flow.
- Order Tracking Page.
- User Profile and Wishlist.

#### 4.1.2 Controller Layer
Manages user interactions and forwards requests to backend services:
- Product Search Controller.
- Cart and Wishlist Controller.
- Checkout Controller.
- User Account Controller.

#### 4.1.3 Service Layer
Implements business logic:
- Search and filter operations.
- Product availability checks.
- Order validation and processing.

---

### 4.2 Backend System

#### 4.2.1 API Gateway
Central entry point for frontend requests, forwarding them to respective microservices.

#### 4.2.2 Authentication Service
Handles:
- User registration and login.
- Password recovery.
- Multi-factor authentication (MFA).

#### 4.2.3 Product Catalog Service
Handles:
- Product listing, search, and filters.
- Inventory updates from sellers.
- Category and tag management.

#### 4.2.4 Order Management Service
Manages:
- Order creation and status tracking.
- Communication with courier services.
- Returns and refunds processing.

#### 4.2.5 Payment Service
Handles:
- Secure payment processing via external gateways.
- Storing payment history for customers and sellers.

#### 4.2.6 Notification Service
Sends:
- Order confirmations and status updates.
- Promotional emails and SMS alerts.

#### 4.2.7 Recommendation Engine
Uses machine learning to suggest products based on:
- User purchase history.
- Browsing behavior and preferences.

---

## 5. Database Design

![database design](https://github.com/user-attachments/assets/1a4ffe93-01d7-4155-ac43-dc8307bf9104)


### Schema Overview:
- **Users Table**: Stores customer and seller details.
- **Products Table**: Stores product details, categories, and inventory levels.
- **Orders Table**: Stores order details, statuses, and payment references.
- **Payments Table**: Logs payment transactions.
- **Reviews Table**: Stores user reviews and ratings for products.

---

## 6. Interface Design
![api design](https://github.com/user-attachments/assets/325390b1-5d6a-4ae6-97fa-64f3be07892f)

### 6.1 API Endpoints

#### Example Endpoints:
| **Endpoint**                | **Method** | **Description**                  |
|-----------------------------|------------|----------------------------------|
| `/api/auth/login`           | POST       | Login user.                     |
| `/api/products`             | GET        | Fetch all products.             |
| `/api/products/{id}`        | GET        | Fetch product by ID.            |
| `/api/cart`                 | POST       | Add product to cart.            |
| `/api/orders`               | POST       | Place an order.                 |
| `/api/orders/{id}/status`   | GET        | Get order status.               |



![notification flow digram](https://github.com/user-attachments/assets/5ef853b2-24d1-4773-b99a-4878c8266acc)

### 6.2 External Interfaces
- **Payment Gateway**: Process payments (e.g., Razorpay, PayPal).
- **Courier Service**: Updates for order delivery status.
- **SMS Gateway**: Sends OTP and notifications.

---

## 7. Non-Functional Requirements

### 7.1 Performance
- Handle 50,000 concurrent users.
- Process up to 1,000 orders per minute.

### 7.2 Scalability
- Scale horizontally with microservices and cloud-native infrastructure.

### 7.3 Availability
- Ensure 99.9% uptime with redundancy in critical components.

### 7.4 Security
- Use encryption for sensitive data (e.g., SSL/TLS, AES for storage).
- Comply with GDPR for user data privacy.

---

## 8. Conclusion

This Software Design Description outlines the architecture, modules, and interfaces for the Flipkart clone e-commerce platform. Its modular design ensures scalability, high availability, and robust security, making it suitable for handling large-scale operations efficiently.
