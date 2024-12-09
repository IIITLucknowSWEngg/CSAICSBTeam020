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


## 4.1. Customer Use Cases

### Use Case 1: Browsing Products
- **Goal**: As a customer, I want to browse products by category, apply filters, and view product details.
- **Preconditions**: User is logged into the application.
- **Postconditions**: User successfully finds products by applying filters and viewing details.
- **Basic Flow**:
  1. User opens the product catalog.
  2. User applies filters (e.g., price, rating, category).
  3. User clicks on a product to view its details.
  
### Use Case 2: Placing an Order
- **Goal**: As a customer, I want to add products to my cart and proceed with checkout.
- **Preconditions**: User is logged in and has added products to the shopping cart.
- **Postconditions**: User has successfully placed the order.
- **Basic Flow**:
  1. User views the cart and clicks "Checkout."
  2. User selects a payment method and enters details.
  3. User receives an email confirmation with the order details.
  4. The order is sent to the delivery agent for processing.

### Use Case 3: Tracking Orders
- **Goal**: As a customer, I want to track the status of my order in real-time.
- **Preconditions**: The customer has placed an order.
- **Postconditions**: The customer is updated with real-time delivery status.
- **Basic Flow**:
  1. User logs into their account.
  2. User navigates to the "Order History" section.
  3. User selects the order they wish to track.
  4. User views real-time updates and the current delivery status.

### Use Case 4: Reviewing Products
- **Goal**: As a customer, I want to leave a review for a product I’ve purchased.
- **Preconditions**: User has purchased a product.
- **Postconditions**: Review is successfully submitted and visible to other customers.
- **Basic Flow**:
  1. User logs into their account.
  2. User navigates to the product they purchased.
  3. User submits a rating and review.

### Use Case 5: Managing Account
- **Goal**: As a customer, I want to update my personal information and preferences.
- **Preconditions**: User is logged in.
- **Postconditions**: User’s information is updated.
- **Basic Flow**:
  1. User logs into their account.
  2. User navigates to the "Account Settings" section.
  3. User updates their profile information (name, email, password, etc.).
  4. User saves changes.

### Use Case 6: Viewing Offers or Discounts
- **Goal**: As a customer, I want to view available offers and discounts on products.
- **Preconditions**: User is logged in.
- **Postconditions**: User is able to see current offers and discounts.
- **Basic Flow**:
  1. User navigates to the "Offers" or "Discounts" section.
  2. User views the list of available offers.

## 4.2. Vendor Use Cases

### Use Case 1: Listing Products
- **Goal**: As a vendor, I want to list products for sale on the platform.
- **Preconditions**: Vendor is logged in.
- **Postconditions**: Product is listed on the platform for sale.
- **Basic Flow**:
  1. Vendor logs into their vendor portal.
  2. Vendor fills in product details (name, description, price, etc.).
  3. Vendor submits the product for review.

### Use Case 2: Updating Product Details
- **Goal**: As a vendor, I want to update details of my listed products.
- **Preconditions**: Vendor is logged in, and product is already listed.
- **Postconditions**: Product details are updated.
- **Basic Flow**:
  1. Vendor logs into their vendor portal.
  2. Vendor selects a product to update.
  3. Vendor modifies the product details (price, description, etc.).
  4. Vendor saves the updated information.

### Use Case 3: Tracking Sales
- **Goal**: As a vendor, I want to track my sales performance.
- **Preconditions**: Vendor is logged in.
- **Postconditions**: Vendor successfully tracks sales and revenue.
- **Basic Flow**:
  1. Vendor logs into their vendor portal.
  2. Vendor navigates to the "Sales" section.
  3. Vendor views the sales report.

### Use Case 4: Managing Inventory
- **Goal**: As a vendor, I want to manage my product inventory (e.g., updating stock levels).
- **Preconditions**: Vendor is logged in.
- **Postconditions**: Vendor successfully updates inventory.
- **Basic Flow**:
  1. Vendor logs into their vendor portal.
  2. Vendor navigates to the product inventory section.
  3. Vendor updates stock levels and availability.
  4. Vendor saves the changes.

## 4.3. Admin Use Cases

### Use Case 1: Processing Orders
- **Goal**: As an admin, I want to process customer orders and resolve issues.
- **Preconditions**: Admin is logged in.
- **Postconditions**: Order is processed, and any issues are resolved.
- **Basic Flow**:
  1. Admin logs into the admin panel.
  2. Admin reviews pending orders.
  3. Admin processes the orders and handles any issues (e.g., cancellations, returns).

### Use Case 2: Handling Returns and Refunds
- **Goal**: As an admin, I want to process product returns and refunds.
- **Preconditions**: Return request has been initiated by a customer.
- **Postconditions**: Return or refund is successfully processed.
- **Basic Flow**:
  1. Admin logs into the admin panel.
  2. Admin reviews return requests.
  3. Admin processes the return or refund and updates the order status.

### Use Case 3: Monitoring Sales
- **Goal**: As an admin, I want to monitor sales and revenue trends across the platform.
- **Preconditions**: Admin is logged in.
- **Postconditions**: Admin has an up-to-date view of platform-wide sales data.
- **Basic Flow**:
  1. Admin logs into the admin panel.
  2. Admin navigates to the "Sales" section.
  3. Admin views the sales and revenue reports.

### Use Case 4: Managing Users
- **Goal**: As an admin, I want to manage user accounts and resolve any issues.
- **Preconditions**: Admin is logged in.
- **Postconditions**: Admin successfully manages user accounts.
- **Basic Flow**:
  1. Admin logs into the admin panel.
  2. Admin views the list of users (customers, vendors, delivery agents).
  3. Admin updates user roles, suspends accounts, or resolves disputes.

### Use Case 5: Generating Reports
- **Goal**: As an admin, I want to generate reports for sales, products, and users.
- **Preconditions**: Admin is logged in.
- **Postconditions**: Admin generates reports.
- **Basic Flow**:
  1. Admin logs into the admin panel.
  2. Admin selects the type of report to generate (sales, inventory, users, etc.).
  3. Admin downloads or views the generated report.

## 4.4. Delivery Agent Use Cases

### Use Case 1: Updating Order Status
- **Goal**: As a delivery agent, I want to update the status of the orders I am delivering.
- **Preconditions**: Delivery agent is logged in.
- **Postconditions**: Order status is updated in real-time.
- **Basic Flow**:
  1. Delivery agent logs into the app.
  2. Delivery agent views the list of orders assigned to them.
  3. Delivery agent updates the status of the order (e.g., "Picked Up," "Out for Delivery," "Delivered").
  
---

These use cases outline the steps and goals for each user group involved in the QuickKart platform. 



## 5. Acceptance Criteria

| Requirement        | Acceptance Criteria                                     |
|--------------------|----------------------------------------------------------|
| Registration       | We can sign up, log in, and reset passwords.             |
| Catalog            | We can browse and filter products.                       |
| Checkout           | We can complete payments securely.                       |
| Order Tracking     | We can track orders in real-time.                        |
| Admin Panel        | Admins can monitor activities and resolve disputes.      |
| Delivery Agent     | Delivery agents can update order status.                |



## 6. Conclusion
This document summarizes the QuickKart Application requirements. By following these guidelines, we will ensure that the platform meets our needs—delivering a secure, easy-to-use, and scalable solution for customers, vendors, admins, and delivery agents.
