# User Requirements Document (URD)

## 1. Introduction

### 1.1 Purpose

We, as the users of the QuickKart Application, need a platform that is easy to use, allowing us to browse, purchase, and manage products seamlessly. The app must be available on both web and mobile devices so that we can access it from anywhere at any time.

### 1.2 Scope

The QuickKart Application should meet the needs of three primary user groups:

- **Customers**: People  who will buy products.
- **Vendors (Sellers)**: Businesses or individuals who will sell products on the platform.
- **Admins**: The people who will manage the platform and ensure everything runs smoothly.

Key features required:

- **User Accounts**: We need to easily sign up, log in, and manage our profiles.
- **Product Catalog**: We want a well-organized catalog to find products easily.
- **Shopping Cart & Checkout**: We need a simple way to add items to our cart and check out securely.
- **Order Management**: We need to track our orders, manage returns, and review order history.
- **Vendor Portal**: Vendors need to manage their products and orders without hassle.
- **Admin Panel**: Admins need a way to monitor activities and resolve issues.
- **Customer Support**: We need an easy way to get help via a chatbot or support tickets.

Delivery services will be entirely managed by third-party logistics providers, who will handle the physical movement of products from vendors to customers.

The platform must be accessible and easy to use, whether we're on a mobile phone, tablet, or desktop.

## 2. Definitions, Acronyms, and Abbreviations

| Term               | Definition                                                   |
|--------------------|--------------------------------------------------------------|
| Product            | Anything for sale on the platform.                           |
| User               | A customer browsing or purchasing products.                  |
| Vendor             | A person or business listing products for sale.              |
| Admin              | A person who manages the platform's operations.              |
| Cart               | A place to store products before purchasing.                 |
| UI                 | How the platform looks and feels to us (User Interface).     |
| UX                 | Our overall experience while using the platform.             |

## 3. Characteristics

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

### 3.3 Admins

- **Who we are**: People who monitor the platform and keep it running smoothly.
- **What we know**: More advanced skills for managing the platform's tools and user interactions.
- **What we need**:
  - Real-time tools to monitor user activity.
  - Access to reports and system performance.
  - A way to handle disputes and moderate content.

## 4. Requirements

### 4.1 Customer Requirements

#### Requirement 1: Browsing Products

- **Goal**: The system must allow customers to browse products by category, apply filters, and view product details.
- **Preconditions**: The customer must be logged into the system.
- **Postconditions**: The customer should successfully find products by applying filters and viewing their details.
- **Description**:
  - Users should be able to open the product catalog.
  - Users should apply various filters (e.g., price, rating, category) to refine their search.
  - Users should be able to select and view detailed information about any product.

#### Requirement 2: Placing an Order

- **Goal**: The system must allow customers to add products to their cart and proceed with checkout.
- **Preconditions**: The customer must be logged in and have products in their shopping cart.
- **Postconditions**: The customer has successfully placed an order.
- **Description**:
  - Users should be able to view their cart and click on "Checkout."
  - Users should choose a payment method and provide the necessary payment information.
  - An order confirmation email should be sent to the customer after placing the order.

#### Requirement 3: Tracking Orders

- **Goal**: The system must allow customers to track the status of their order in real-time.
- **Preconditions**: The customer must have placed an order.
- **Postconditions**: The customer should receive real-time updates about their delivery status.
- **Description**:
  - The customer should be able to log into their account and navigate to "Order History."
  - The system should provide real-time tracking updates via third-party logistics services for the selected order.

#### Requirement 4: Reviewing Products

- **Goal**: The system must allow customers to leave a review for any purchased product.
- **Preconditions**: The customer must have purchased the product.
- **Postconditions**: The review must be successfully submitted and visible to other customers.
- **Description**:
  - Users should log into their account and navigate to the product they purchased.
  - Customers should submit ratings and leave detailed product reviews.

#### Requirement 5: Managing Account

- **Goal**: The system must allow customers to update their personal information and preferences.
- **Preconditions**: The customer must be logged in.
- **Postconditions**: The system should successfully update the customer’s information.
- **Description**:
  - Customers should be able to navigate to "Account Settings."
  - Users can update their profile details, including name, email, and password, and save these changes.

#### Requirement 6: Viewing Offers or Discounts

- **Goal**: The system must allow customers to view available offers and discounts on products.
- **Preconditions**: The customer must be logged in.
- **Postconditions**: The customer should be able to see available offers and discounts.
- **Description**:
  - Users should navigate to the "Offers" or "Discounts" section.
  - Users should be able to view a list of available discounts and offers on products.

### 4.2 Vendor Requirements

#### Requirement 1: Listing Products

- **Goal**: The system must allow vendors to list products for sale.
- **Preconditions**: The vendor must be logged into the platform.
- **Postconditions**: The product is successfully listed on the platform.
- **Description**:
  - Vendors should log into their vendor portal and fill in product details (name, description, price, etc.).
  - Vendors must submit products for review and approval to ensure they meet platform standards.

#### Requirement 2: Updating Product Details

- **Goal**: The system must allow vendors to update the details of their listed products.
- **Preconditions**: The vendor must be logged in and the product must already be listed.
- **Postconditions**: The product details are updated in the system.
- **Description**:
  - Vendors should be able to select a product and modify its information, including price and description.

#### Requirement 3: Tracking Sales

- **Goal**: The system must allow vendors to track their sales performance.
- **Preconditions**: The vendor must be logged in.
- **Postconditions**: The vendor is able to track their sales and view the generated revenue.
- **Description**:
  - Vendors should log into their portal and view sales reports and revenue generated.

#### Requirement 4: Managing Inventory

- **Goal**: The system must allow vendors to manage their product inventory.
- **Preconditions**: The vendor must be logged in.
- **Postconditions**: The vendor’s inventory is successfully updated.
- **Description**:
  - Vendors should be able to update stock levels and availability for their listed products.

### 4.3 Admin Requirements

#### Requirement 1: Processing Orders

- **Goal**: The system must allow admins to process customer orders and resolve issues.
- **Preconditions**: The admin must be logged in.
- **Postconditions**: The order is processed, and any issues are resolved.
- **Description**:
  - Admins should log into the admin panel, review pending orders, and process them.
  - They are responsible for resolving any issues such as cancellations, returns, or inventory mismatches.

#### Requirement 2: Handling Returns and Refunds

- **Goal**: The system must allow admins to process product returns and issue refunds.
- **Preconditions**: A return request has been initiated by the customer.
- **Postconditions**: The return or refund is successfully processed.
- **Description**:
  - Admins should log into the admin panel and review return requests from customers.
  - Admins can approve and process the return or refund and update the order status.

#### Requirement 3: Monitoring Sales

- **Goal**: The system must allow admins to monitor sales and revenue across the platform.
- **Preconditions**: The admin must be logged in.
- **Postconditions**: Admin will have an up-to-date overview of platform-wide sales data.
- **Description**:
  - Admins should navigate to the "Sales" section in the admin panel and view comprehensive sales and revenue reports.

#### Requirement 4: Managing Users

- **Goal**: The system must allow admins to manage user accounts and resolve related issues.
- **Preconditions**: The admin must be logged in.
- **Postconditions**: Admin successfully manages user accounts.
- **Description**:
  - Admins can view customer and vendor user lists.
  - Admins can modify roles, suspend accounts, or resolve disputes, such as user complaints.

#### Requirement 5: Generating Reports

- **Goal**: The system must allow admins to generate reports for sales, products, and user activity.
- **Preconditions**: The admin must be logged in.
- **Postconditions**: The system generates the selected report.
- **Description**:
  - Admins should be able to generate and download reports for various data types, such as sales, user activities, or product information.

## 5. Acceptance Criteria

| Requirement        | Acceptance Criteria                                     |
|--------------------|----------------------------------------------------------|
| Registration       | We can sign up, log in, and reset passwords.             |
| Catalog            | We can browse and filter products.                       |
| Checkout           | We can complete payments securely.                       |
| Order Tracking     | We can track orders in real-time via third-party services.|
| Admin Panel        | Admins can monitor activities and resolve disputes.      |
| Vendor Portal      | Vendors can manage products and orders.                  |

## 6. Conclusion

This document summarizes the QuickKart Application requirements. By following these guidelines, we will ensure that the platform meets our needs—delivering a secure, easy-to-use, and scalable solution for customers, vendors, and admins, with delivery services fully outsourced to third-party logistics providers.
