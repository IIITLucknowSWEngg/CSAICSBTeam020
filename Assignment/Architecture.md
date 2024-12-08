# Flipkart Clone Architecture

## 1. System Context Diagram

```plantuml
@startuml
title System Context Diagram - Flipkart Clone

actor "Users" as U
actor "Sellers" as S
actor "Delivery Agents" as D

package "Flipkart Clone" {
  rectangle "Web & Mobile Application" as App
}

rectangle "Payment Gateway Service" as PGS
rectangle "Banking Services" as Bank
rectangle "Logistics Management Service" as LMS
rectangle "Third-Party Analytics Service" as Analytics
rectangle "External Inventory Management System" as Inventory

U --> App : Browse, Search, \nPurchase Products
S --> App : List & Manage \nProducts
D --> App : Update Delivery \nStatus

App --> PGS : Process Payments
PGS --> Bank : Process Transactions
App --> LMS : Manage Delivery \nLogistics
App --> Analytics : Track User Activities
App --> Inventory : Sync Product Details

@enduml
```

![system_context_diagram](https://github.com/user-attachments/assets/e15149a9-95ef-459e-8215-83679f7d5e2f)

The System Context Diagram provides an overview of how users and external systems interact with the application. Key external actors include:

- **Customers**: Browse products, place orders, and track deliveries.
- **Sellers**: Manage inventory, list products, and process orders.
- **Delivery Agents**: Handle and track deliveries, with the delivery process completely managed by third-party services.
- **Third-party APIs**: Integrate with payment gateways, logistics providers, and marketing platforms. These APIs manage payments, delivery assignments, and tracking, as well as external services for promotions and other features.

---

## 2. Container Diagram  

The Container Diagram outlines the primary containers within the Flipkart Clone, divided into **User**, **Seller**, and **Admin** roles:  

### **User**
```plantuml
@startuml
title Flipkart Clone System

actor User
actor Admin

package "Flipkart Clone System" {
  rectangle "«Application» Mobile App" as MobileApp
  rectangle "«Application» Web App" as WebApp
  rectangle "«API» User API Gateway" as APIGateway

  database "«Database» User Database" as UserDB
  database "«Database» Product Database" as ProductDB
  database "«Database» Order Database" as OrderDB
  database "«Database» Cart Database" as CartDB
  database "«Database» Payment Database" as PaymentDB

  rectangle "«External System» External Image Storage" as ImageStorage
  rectangle "«External System» Payment Gateway" as PaymentGateway
  rectangle "«External System» Push Notification Service" as PushService
  rectangle "«External System» Analytics Service" as AnalyticsService
}

User --> MobileApp : Use Mobile App
User --> WebApp : Use Web App
Admin --> APIGateway : Manage Inventory & Orders

MobileApp --> APIGateway : API Calls
WebApp --> APIGateway : API Calls

APIGateway --> UserDB : Manage User Data
APIGateway --> ProductDB : Fetch/Search Products
APIGateway --> ProductDB : Update Inventory
APIGateway --> OrderDB : Manage Orders
APIGateway --> CartDB : Manage Cart
APIGateway --> PaymentDB : Process Payments

APIGateway --> ImageStorage : Upload Product Images
APIGateway --> PaymentGateway : Process Payments
APIGateway --> PushService : Send Push Notifications
APIGateway --> AnalyticsService : Track User Activities

@enduml
```

![Container_diagram](https://github.com/user-attachments/assets/74cb52ad-ef32-4a04-b883-8711a82101e4)  

- **Web and Mobile Applications**: User interfaces for browsing products, placing orders, and managing accounts.  
- **Backend Services**: Handles business logic, user authentication, order tracking, and personalized recommendations.  
- **Databases**: Stores data related to user accounts, order history, preferences, and payment details.  

### **Seller**
```plantuml
@startuml
!define RECTANGLE rect
skinparam componentStyle rectangle

title Flipkart Clone System - Seller Module

actor Seller
actor Admin

Seller --> "«Application»\nSeller Portal - Mobile App" : Access Mobile App
Seller --> "«Application»\nSeller Portal - Web App" : Access Web App

Admin --> "«API»\nSeller API Gateway" : Monitor Seller Activities

"«Application»\nSeller Portal - Mobile App" --> "«API»\nSeller API Gateway" : API Calls
"«Application»\nSeller Portal - Web App" --> "«API»\nSeller API Gateway" : API Calls

"«API»\nSeller API Gateway" --> "«Database»\nSeller Database" : Manage Seller Profiles
"«API»\nSeller API Gateway" --> "«Database»\nProduct Database" : Manage Product Listings
"«API»\nSeller API Gateway" --> "«Database»\nOrder Database" : Track Orders & Sales
"«API»\nSeller API Gateway" --> "«External System»\nExternal Analytics Service" : Analyze Sales Data
"«API»\nSeller API Gateway" --> "«External System»\nPayment Reconciliation System" : Reconcile Payments

@enduml
```

![seller](https://github.com/user-attachments/assets/a6e8cf3f-fcd0-435a-ae6e-91cca1532f95)

- **Seller Dashboard (Web/Mobile)**: Interface for managing product listings, inventory, and order fulfillment.  
- **Backend Services**: Handles inventory management, order processing, seller performance analytics, and catalog updates.  
- **Databases**: Stores seller data, product information, stock levels, and sales data.  

### **Admin**
```plantuml
@startuml
!define RECTANGLE rect
skinparam componentStyle rectangle

title Flipkart Clone System - Admin Module

actor Admin

Admin --> "«Application»\nAdmin Portal - Web App" : Access Admin Portal
"«Application»\nAdmin Portal - Web App" --> "«API»\nAdmin API Gateway" : API Calls

"«API»\nAdmin API Gateway" --> "«Database»\nUser Database" : Manage Users
"«API»\nAdmin API Gateway" --> "«Database»\nSeller Database" : Monitor Sellers
"«API»\nAdmin API Gateway" --> "«Database»\nOrder Database" : Review Order Data
"«API»\nAdmin API Gateway" --> "«Database»\nProduct Database" : Audit Product Listings
"«API»\nAdmin API Gateway" --> "«Database»\nReport Database" : Generate Reports
"«API»\nAdmin API Gateway" --> "«External System»\nFraud Detection Service" : Check for Fraudulent Activities
"«API»\nAdmin API Gateway" --> "«External System»\nNotification System" : Send Admin Notifications
"«API»\nAdmin API Gateway" --> "«External System»\nAnalytics Service" : Analyze Platform Data

@enduml
```

![admin](https://github.com/user-attachments/assets/a9a2f4bf-10e0-4a31-952e-a532f7b590ad)

- **Admin Dashboard (Web)**: Interface for monitoring user activity, managing vendors, resolving disputes, and generating reports.  
- **Backend Services**: Handles user management, vendor approvals, platform health monitoring, and reporting.  
- **Databases**: Stores administrative data, user/vendor records, transaction logs, and complaint histories.  

---

## 3. Component Diagram

![component](https://github.com/user-attachments/assets/3a07ba8c-3e3c-461e-9a75-a474981340e1)

The Component Diagram focuses on core functionalities for customers, sellers, and delivery agents:  

### For Customers

- **Product Browsing and Search**: Enable users to search, filter, and browse products.  
- **Cart Management**: Handles adding/removing items from the cart.  
- **Order Management**: Supports placing orders, payments, and tracking deliveries.  
- **Recommendations**: Provides personalized product recommendations based on browsing and purchase history.  

### For Sellers

- **Product Listing Management**: Allows sellers to add, update, and remove product listings.  
- **Inventory Management**: Tracks stock levels for listed products.  
- **Order Processing**: Manages order acceptance and shipment preparation.  

### For Delivery Agents

- **Delivery Assignment**: The assignment of orders to delivery agents based on location and availability is completely handled by third-party services.
- **Delivery Tracking**: Real-time tracking of deliveries is also managed by third-party services.

---

## 4. Deployment Diagram

![deployement 1](https://github.com/user-attachments/assets/f3c20f37-d96a-4e34-a2ac-15479fea8f7a)

The Deployment Diagram outlines the architecture of the Flipkart Clone, highlighting the interaction between its components and third-party services.

## Key Components

### 1. **User, Seller, and Admin Devices**

- **Users**: Access via web and mobile apps to browse products, place orders, and track deliveries.  
- **Sellers**: Use the seller app to manage product listings and orders.  
- **Admins**: Oversee inventory, users, and analytics via the Admin Dashboard.

### 2. **Load Balancers**

- Distribute user requests across backend servers for high availability and scalability.

### 3. **Backend Servers**

- Microservices handle:
  - **User Management**: Authentication and profile management.
  - **Product Search**: Browse and search for items.
  - **Order Management**: Process and update orders.
  - **Recommendations**: Generate personalized product suggestions.
  - **Payments**: Handle secure transactions.

### 4. **Databases**

- Store data for:
  - **Users**: Profiles and account details.
  - **Products**: Listings and pricing.
  - **Orders**: Payment and delivery status.
  - **Analytics**: Metrics for insights.

### 5. **Third-Party Services**

- **Payment Gateway**: For secure payments.  
- **Logistics API**: To handle shipping and delivery.  
- **Social Media APIs**: For marketing and sharing deals.  
- **Cloud Storage**: For static assets like product images.

### 6. **Content Delivery Network (CDN)**

- Speeds up delivery of static assets for a seamless user experience.

## Summary

The architecture ensures scalability, reliability, and seamless operations for users, sellers, and admins, with efficient integrations for payments, logistics, and content delivery.

