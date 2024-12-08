# **Software Requirements Specification (SRS)**

## **Project Title: QuickKart**
**Version:** 1.0  
**Date:** [Insert Date]  

---

## **1. Introduction**

### **1.1 Purpose**
The purpose of this Software Requirements Specification (SRS) document is to define the functional, non-functional, and system requirements for **QuickKart**, an e-commerce platform similar to Flipkart. This platform will facilitate online shopping, allowing users to browse, search, and purchase products while enabling sellers to list and manage their inventory. An admin dashboard will allow administrators to moderate platform activities. 

### **1.2 Scope**
The QuickKart e-commerce platform aims to provide:  
- **User Features:** Product browsing, filtering, and searching; shopping cart; secure payments; order tracking.  
- **Seller Features:** Product listing, inventory management, and sales tracking.  
- **Admin Features:** User, product, and order moderation; platform analytics and reports.  

The platform will support web browsers and mobile devices, ensuring a seamless shopping experience. It will integrate secure payment gateways like **PayPal, Stripe, and UPI** for payment processing. 

### **1.3 Definitions, Acronyms, and Abbreviations**
- **SRS**: Software Requirements Specification  
- **UI**: User Interface  
- **UX**: User Experience  
- **SKU**: Stock Keeping Unit  
- **API**: Application Programming Interface  

### **1.4 References**
- [E-commerce Design Best Practices](https://www.forbes.com/advisor/business/ecommerce-website-design/)  
- [REST API Best Practices](https://www.freecodecamp.org/news/rest-api-best-practices-rest-endpoint-design-examples/)  
- [Payment Gateway Integration Guide](https://medium.com/@vaniukov.s/online-payment-gateway-integration-a-thorough-guide-993c794b65b9)  

---

## **2. Overall Description**

### **2.1 Product Perspective**
The QuickKart system is a web and mobile application for online shopping. It allows users to browse, search, and buy products, while sellers can list and manage their products. The system will have **three types of users**:  
1. **Users (Shoppers)**: Browse and purchase products.  
2. **Sellers**: Add products and manage inventory.  
3. **Admins**: Oversee platform activity, user accounts, and transactions.  

### **2.2 Product Functions**
- **User Functions**:  
  - User registration, login, and profile management.  
  - Product browsing, search, and filter.  
  - Add to cart, checkout, and make payments.  
  - View order history and track orders.  

- **Seller Functions**:  
  - Add, edit, and delete product listings.  
  - Manage inventory and track orders.  

- **Admin Functions**:  
  - Manage users, sellers, and products.  
  - Approve or reject seller product listings.  
  - View platform analytics and reports.  

### **2.3 User Classes and Characteristics**
1. **Users (Shoppers)**: Browse, search, and purchase products.  
2. **Sellers**: List and manage their product inventory.  
3. **Admins**: Manage user accounts, moderate products, and ensure compliance.  

### **2.4 Operating Environment**
- **Frontend**: HTML, CSS, JavaScript, React (web) / React Native (mobile).  
- **Backend**: Node.js, Express, REST APIs for business logic.  
- **Database**: MySQL for relational data (users, products, orders).  
- **Payment Integration**: Stripe, PayPal, and UPI.  

### **2.5 Design and Implementation Constraints**
- Mobile responsiveness for users on all devices.  
- Fast page load times (<3 seconds) for product pages.  
- Secure payment processing that complies with **PCI-DSS standards**.  

---

## **3. Specific Requirements**

### **3.1 Functional Requirements**

**1. User Registration and Login**  
- Users can register using email, phone number, or social media login.  
- Passwords must be stored securely (using **bcrypt hashing**).  
- Two-factor authentication (2FA) for added security.  

**2. Product Browsing, Search, and Filter**  
- Users can browse products by categories, price, and ratings.  
- Users can search using a search bar with autocomplete functionality.  

**3. Shopping Cart**  
- Users can add products to the cart and update the quantity.  
- Cart details (price, quantity) must be displayed clearly.  

**4. Checkout and Payments**  
- Users can choose shipping addresses and payment methods.  
- Secure payments via **Stripe, PayPal, and UPI** payment gateways.  

**5. Order Management**  
- Users can view, cancel, and track orders.  
- Admins can view and moderate order disputes.  

**6. Seller Dashboard**  
- Sellers can add, edit, and delete products.  
- Sellers can track orders and view product sales data.  

**7. Admin Panel**  
- Admins can manage users, sellers, products, and orders.  
- Admins can approve or reject seller product listings.  

---

### **3.2 Non-Functional Requirements**

**1. Performance**  
- The system must support up to **50,000 concurrent users**.  
- Product pages should load in under **3 seconds**.  

**2. Scalability**  
- Support horizontal scaling of the system as traffic grows.  

**3. Security**  
- Use **AES-256** encryption for sensitive data at rest.  
- Implement **two-factor authentication** for user accounts.  

**4. Usability**  
- Mobile-responsive design.  
- Intuitive user interface for all classes of users.  

**5. Reliability**  
- Ensure **99.9% uptime** for essential services.  
- Automated backups for disaster recovery.  

**6. Maintainability**  
- Use modular and maintainable code with clear documentation.  
- Changes in one module should not affect others.  

**7. Compliance**  
- Comply with **GDPR** for user privacy and **PCI-DSS** for payments.  

---

## **4. Interfaces**

### **4.1 Hardware Interfaces**
- **Mobile Devices**: Support iOS and Android devices.  
- **Web Browsers**: Support Chrome, Firefox, and Safari.  

### **4.2 Software Interfaces**
- **Payment Gateway APIs**: Integrate **Stripe, PayPal, and UPI**.  
- **Third-party APIs**: APIs for geolocation, search suggestions, etc.  

### **4.3 Communication Interfaces**
- **HTTP/HTTPS** for secure web traffic.  
- **REST APIs** for frontend-backend communication.  
- **WebSockets** for real-time notifications.  

---

## **5. System Features**

### **5.1 Use Case Diagram**

![usecase 1](https://github.com/user-attachments/assets/354c47fc-d734-4408-aedd-d3d946facee2)

### **5.2 Abuse Case Diagram**
![abuse case 1](https://github.com/user-attachments/assets/f358a3d2-a4d7-40ff-82ae-13e91443425d)


### **5.3 Error Case Diagram**
![bLR1Rjim3BtxAuZiN2pOgGYAebso00NMjMYx3z1i9XKYIu4efmY6_ViaqmxCgiuydzn7FfBX8-dUK50-DBKf36u210TURry3LDfZ6RIp1UsqtIklQcW8IqK8lmk8prTLxhRUDRPQEkFyrTKtxvs_lePFw_KgFXyxhN23blG1a-DokLulb-peV8K-ZpIFZt38eypdbvUTqzhPC1w3pUSZF76jtg](https://github.com/user-attachments/assets/809a8270-2230-4e79-8fc8-69df3adac8d7)


---

## **6. Other Requirements**

### **6.1 Localization**
- Support for multiple languages and currencies.  
- Display date/time based on user’s locale.  

### **6.2 Ethical Requirements**
- Enforce moderation to prevent illegal/inappropriate product listings.  

---

## **7. Appendices**

### **Appendix A: Glossary of Terms**
- **User**: A shopper browsing and buying products.  
- **Seller**: A user listing and selling products.  
- **Admin**: A platform moderator managing users, orders, and disputes.  

### **Appendix B: Assumptions and Dependencies**
- The system assumes stable internet access for users.  
- Integration with third-party APIs like **Stripe and PayPal** is required.  

---
## **8. System Architecture**

The system architecture for the **QuickKart** platform is designed to ensure scalability, maintainability, and efficiency. The architecture is divided into **frontend**, **backend**, **database**, and **payment gateway** components, each with a specific role.

### **1. Frontend**
- **Technologies**: 
  - **Web Application**: HTML, CSS, JavaScript, and **React.js** for building an interactive, dynamic, and responsive user interface.  
  - **Mobile Application**: **React Native** is used to create a cross-platform mobile app that works on both Android and iOS.  
- **Role**:  
  - Handles user interactions such as browsing products, adding them to the cart, and managing user accounts.  
  - Provides a smooth and intuitive user experience with responsive design for mobile, tablet, and desktop devices.  
  - Communicates with the backend via **REST APIs** to retrieve or send data (e.g., user login, product details, or order placement).  

---

### **2. Backend**
- **Technologies**: **Node.js** (runtime), **Express.js** (web framework)  
- **Role**:  
  - Acts as the central control unit that processes user requests, manages business logic, and communicates with the database.  
  - Exposes **REST APIs** that facilitate data flow between the frontend and backend.  
  - Handles crucial operations like user authentication, product listings, inventory management, order processing, and notifications.  
  - Integrates with third-party services, including payment gateways and notification services.  

---

### **3. Database**
- **Technology**: **MySQL** (Relational Database)  
- **Role**:  
  - Stores and manages all platform data, including:  
    - **User Data**: Usernames, passwords, shipping addresses, payment preferences, etc.  
    - **Product Data**: Product details (name, description, images, price, stock availability, SKUs, categories).  
    - **Order Data**: Order history, payment status, shipping details, and transaction logs.  
    - **Seller Data**: Details related to sellers, their product listings, and order details.  
  - Ensures **data integrity and consistency** across all system modules.  
  - Supports efficient **query optimization** to ensure fast data retrieval, especially during searches and order tracking.  

---

### **4. Payment Gateway**
- **Technologies**: **Stripe**, **PayPal**, and **UPI** (Unified Payments Interface)  
- **Role**:  
  - Manages secure payment processing by facilitating payments from users to sellers.  
  - Supports multiple payment methods such as credit/debit cards, UPI, PayPal, and digital wallets.  
  - Ensures that all payment data is encrypted during transmission using **TLS/SSL** protocols to prevent unauthorized access.  
  - Adheres to **PCI-DSS** (Payment Card Industry Data Security Standards) to ensure the security of payment transactions.  

---

### **System Flow (Simplified)**
1. **User Interaction**: A user browses the frontend (web or mobile) and selects products to purchase.  
2. **API Request**: The frontend sends a request to the backend via **REST APIs**.  
3. **Backend Processing**: The backend processes the request, interacts with the database (MySQL) to retrieve or update product, user, or order information.  
4. **Response to Frontend**: The backend returns the requested data (e.g., product details, cart updates) to the frontend.  
5. **Payment Gateway**: When users check out, payment details are sent to **Stripe/PayPal/UPI** via secure payment APIs, and the status of the payment is updated in the database.  
6. **Order Confirmation**: Once the payment is successful, an order is created, and the order details are stored in the MySQL database. Notifications are sent to the user and seller about the order status.  

This architecture ensures a **seamless shopping experience**, supports **real-time order tracking**, and enables the platform to handle high traffic during peak sales events.

---
