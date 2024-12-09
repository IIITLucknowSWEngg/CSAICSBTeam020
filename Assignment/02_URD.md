# User Requirements Document (URD)

## 1. Introduction

### 1.1 Purpose
We, as the users of the QuickKart Application, need a platform that is easy to use, allowing us to browse, purchase, and manage products seamlessly. The app must be available on both web and mobile devices so that we can access it from anywhere at any time.

### 1.2 Scope
The QuickKart Application should meet the needs of four primary user groups:

- **Customers**: People like me who will buy products.
- **Vendors (Sellers)**: Businesses or individuals who will sell products on the platform.
- **Admins**: The people who will manage the platform and ensure everything runs smoothly.
- **Delivery Agents**: The ones who will physically deliver the products to us, the customers.

We need these key features to be part of the application:

- **User Accounts**: We need to easily sign up, log in, and manage our profiles.
- **Product Catalog**: We want a well-organized catalog to find products easily.
- **Shopping Cart & Checkout**: We need a simple way to add items to our cart and check out securely.
- **Order Management**: We need to track our orders, manage returns, and review order history.
- **Vendor Portal**: Vendors need to manage their products and orders without hassle.
- **Admin Panel**: Admins need a way to monitor activities and resolve issues.
- **Customer Support**: We need an easy way to get help via a chatbot or support tickets.
- **Delivery Management**: The delivery agents need to get real-time updates on orders and routes.

The platform must be accessible and easy to use, whether we're on a mobile phone, tablet, or desktop.

## 2. Definitions, Acronyms, and Abbreviations

| Term               | Definition                                                   |
|--------------------|--------------------------------------------------------------|
| Product            | Anything for sale on the platform.                           |
| User               | A customer browsing or purchasing products.                  |
| Vendor             | A person or business listing products for sale.              |
| Admin              | A person who manages the platform's operations.              |
| Delivery Agent     | The person responsible for delivering the order.             |
| Cart               | A place to store products before purchasing.                 |
| UI                 | How the platform looks and feels to us (User Interface).     |
| UX                 | Our overall experience while using the platform.             |

## 3.Characteristics

### 3.1 Customers
- **Who we are**: Anyone who wants to buy products for personal or business use.
- **What we know**: Basic knowledge of browsing on mobile apps and websites.
- **What we need**:
  - Easy-to-use search and filter to find products.
  - Fast and secure checkout process.
  - Real-time updates on order status.
  - Notifications about deals and promotions.

### 3.2 Vendors (Sellers)
- **Who we are**: Businesses or people listing products for sale.
- **What we know**: Some experience with online tools like dashboards.
- **What we need**:
  - A simple way to list products and update details.
  - Tools to manage inventory, sales, and orders.
  - Support for managing returns and refunds.
  - Communication tools to work with delivery agents for shipping.

### 3.3 Admins
- **Who we are**: People who monitor the platform and keep it running smoothly.
- **What we know**: More advanced skills for managing the platform's tools and user interactions.
- **What we need**:
  - Real-time tools to monitor user activity.
  - Access to reports and system performance.
  - A way to handle disputes and moderate content.

### 3.4 Delivery Agents
- **Who we are**: People or companies that deliver the products to customers.
- **What we know**: Basic knowledge of delivery apps.
- **What we need**:
  - Clear instructions for deliveries.
  - Route optimization for faster deliveries.
  - A way to update the status of deliveries.

## 4. Use Cases

### Use Case 1: Browsing Products (Customer)
- **Goal**: I want to browse through categories, use filters, and find products I like.
- **Steps**:
  1. I open the product catalog.
  2. I use filters like price or rating.
  3. I select a product and see its details.

### Use Case 2: Placing an Order (Customer)
- **Goal**: I want to add products to my cart and checkout quickly.
- **Steps**:
  1. I go to my cart and click "Checkout."
  2. I choose my payment method and enter the details.
  3. My order is confirmed, and I get an email with details.
  4. The delivery agent takes care of my order.

### Use Case 3: Listing Products (Vendor)
- **Goal**: I want to list my products easily so customers can buy them.
- **Steps**:
  1. I log into my vendor portal.
  2. I add my product details (name, price, description, etc.).
  3. I submit the product for review.

### Use Case 4: Resolving Disputes (Admin)
- **Goal**: I want to handle disputes between customers and vendors efficiently.
- **Steps**:
  1. I see the details of the dispute.
  2. I contact both parties.
  3. I resolve the issue and update the system.

### Use Case 5: Updating Order Status (Delivery Agent)
- **Goal**: I want to update my order’s status as I deliver it.
- **Steps**:
  1. I log into the app.
  2. I pick up the order and update the status.
  3. I continue to update as the order moves along its route.

## 5. Functional Requirements

### 5.1 User Registration & Authentication
- **Customer**: Login via email, Google, or Facebook.
- **Vendor**: Registration with business details and GSTIN.
- **Admin**: Admin credentials with two-factor authentication.
- **Delivery Agent**: Account for delivery updates.

### 5.2 Product Catalog
- **Customer**: Browse, filter, and view product details.
- **Vendor**: List, update, or remove products.

### 5.3 Shopping Cart & Checkout
- **Customer**: Add/remove products, view total, apply coupons, choose payment methods.

### 5.4 Order Management
- **Customer**: View order history, cancel or return orders.
- **Vendor**: View and manage customer orders.
- **Delivery Agent**: Update order status.

## 6. Non-Functional Requirements

### 6.1 Performance
- The app should load in 3 seconds under normal conditions.
- It should support 50,000+ users at the same time.

### 6.2 Security
- **Data Security**: All personal and payment data must be encrypted.
- **Fraud Prevention**: Use tools to detect fraudulent transactions.

### 6.3 Scalability
- The system should be able to grow as more users and products join.

### 6.4 Usability
- The platform should work seamlessly on mobile, tablet, and desktop.
- **Accessibility**: We need features like screen reader support for users with disabilities.

## 7. Assumptions & Dependencies

- **Third-Party APIs**: Payment gateways (Razorpay, PayPal), Firebase for notifications.
- **Delivery Agents**: Integration with third-party delivery services.
- **Internet**: A stable internet connection is required.

## 8. Acceptance Criteria

| Requirement        | Acceptance Criteria                                     |
|--------------------|----------------------------------------------------------|
| Registration       | We can sign up, log in, and reset passwords.             |
| Catalog            | We can browse and filter products.                       |
| Checkout           | We can complete payments securely.                       |
| Order Tracking     | We can track orders in real-time.                        |
| Admin Panel        | Admins can monitor activities and resolve disputes.      |
| Delivery Agent     | Delivery agents can update order status.                |

## 9. Risks

| Risk               | Mitigation                                                 |
|--------------------|------------------------------------------------------------|
| Data Breach        | Regular security audits and encryption.                   |
| Payment Failure    | Use backup payment gateways.                              |
| Vendor Abuse       | Perform KYC checks for vendors.                           |
| Delivery Delays    | Real-time tracking and notifications.                     |

## 10. Conclusion
This document summarizes the QuickKart Application requirements. By following these guidelines, we will ensure that the platform meets our needs—delivering a secure, easy-to-use, and scalable solution for customers, vendors, admins, and delivery agents.
