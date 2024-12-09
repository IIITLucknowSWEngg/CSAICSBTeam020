## **Cross-reference Matrix** for the **QuickKart (Flipkart Clone)**

### Stakeholder Requirements Mapping

| **Stakeholder**             | **URD Section Number** | **URD Topic**             | **SRS Section Number** | **SRS Topic**               | **Architecture Section** | **Architecture Topic**           | **Design Section Number** | **Design Topic**                 | **Test Section Number** | **Test Topics**                        |
|-----------------------------|------------------------|---------------------------|------------------------|-----------------------------|--------------------------|----------------------------------|----------------------------|-----------------------------------|------------------------|---------------------------------------|
| **End User (Customer)**      | 3.1                    | User Login & Registration  | 3.1.1                  | User Registration and Login  | 1                        | Authentication Service            | 4.2.2                      | Authentication Service             | TC-REG-001              | Validate user registration functionality. |
|                             | 3.1(Use Case 1)                    | Browse Products            | 3.1.2                  | Product Browsing, Search, and Filter | 1                        | Product Catalog Service           | 4.2.3                      | Product Catalog Service            | TC-PRODUCTS-003         | Validate product listing display.     |
|                             | 3.1                    | Add to Cart                | 3.1.3                  | Shopping Cart                | 1                        | Shopping Cart Service             | 4.1.1                      | Shopping Cart and Wishlist          | TC-CART-004             | Validate add/remove from cart.        |
|                             | 3.1(Use Case 2)                    | Checkout                   | 3.1.4                  | Checkout and Payments        | 1                        | Payment Integration               | 4.2.5                      | Payment Service                    | TC-ORDER-005            | Validate checkout flow.              |
|                             | 3.1                    | Track Order                | 3.1.5                  | Order Management             | 1                        | Order Management Service          | 4.2.4                      | Order Management Service           | TC-TRACK-005            | Validate order tracking functionality. |
| **Seller/Vendor**            | 3.2                    | Add New Product            | 3.1.6                  | Product Management           | 1                        | Product Catalog Service           | 4.2.3                      | Product Management                 | TC-SELLER-ADD-PRODUCT-007 | Validate product upload process.     |
|                             | 3.2                    | Manage Inventory           | 3.1.7                  | Inventory Management         | 1                        | Inventory Management Service      | 4.2.3                      | Product Management                 | TC-SELLER-MANAGE-ORDER-008 | Validate inventory updates.          |
| **Delivery Partner**         | 3.4                    | Update Delivery Status     | 3.1.8                  | Delivery Integration         | 1                        | Delivery API Integration          | 4.2.4                      | Order Management Service           | TC-DELIVERY-010         | Validate delivery status updates.    |
| **Admin**                    | 3.3                    | Admin Dashboard            | 3.1.9                  | Admin Panel                  | 1                        | Admin Services                    | 4.2.2                      | Admin Dashboard                    | TC-ADMIN-MANAGE-USERS-009 | Validate admin dashboard functionality. |
| **Internal Team (Developers)** | 4.1                    | System Architecture Overview | 2.4                    | Operating Environment        | 1                        | Backend Service Architecture      | 4.2.1                      | API Gateway                        | TC-ARCH-010             | Validate system architecture integration. |
| **Non-Functional Requirements** |                        | Performance & Security     | 2.5                    | Design and Implementation Constraints | 1                        | Load Balancer & Security Measures | 7.1                        | Performance                        | TC-NFR-011             | Test system performance & security.  |

### API Call Mapping

| **Stakeholder/Actor**   | **Step**                                     | **API Call(s)**                | **Module/Service**         |
|-------------------------|----------------------------------------------|--------------------------------|----------------------------|
| User                    | Open the registration page                   | `GET /api/register`            | Registration               |
| User                    | Enter valid information (name, email, password) | `POST /api/register`           | User Management            |
| User                    | Submit the registration form                 | `POST /api/register`           | User Management            |
| User                    | Open the login page                          | `GET /api/login`               | Login                      |
| User                    | Enter valid email and password               | `POST /api/login`              | Authentication             |
| User                    | Submit the login form                        | `POST /api/login`              | Authentication             |
| User                    | Navigate to the "Products" section           | `GET /api/products`            | Product Management         |
| User                    | Click the "Add to Cart" button               | `POST /api/cart/add`           | Cart                       |
| User                    | Go to the cart and click "Place Order"       | `POST /api/order/place`        | Order Management           |
| Seller                  | Enter seller details                         | `POST /api/seller/register`    | Seller Management          |
| Seller                  | Submit the registration form                 | `POST /api/seller/register`    | Seller Management          |
| Seller                  | Enter product details                        | `POST /api/product/add`        | Product Management         |
| Seller                  | Submit the product listing                   | `POST /api/product/add`        | Product Management         |
| Seller                  | Go to "Orders" section                       | `GET /api/orders`              | Order Management           |
| Seller                  | Update order status to "Shipped"             | `PUT /api/order/{orderId}`     | Order Management           |
| Admin                   | Navigate to the "Users" section              | `GET /api/users`               | User Management            |
| Delivery API            | Trigger the third-party delivery API         | `GET /api/delivery/{orderId}`  | Delivery API               |
| Payment API             | Trigger the payment API                     | `POST /api/payment/process`    | Payment API                |
| Maps API                | Trigger the maps API with shipping address   | `GET /api/maps/geocode`        | Maps API                   |

---