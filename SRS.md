# **Software Requirements Specification (SRS)**

## **Project Title: QuickKart**
**Version:** 1.0  


---

## **1. Introduction**

### **1.1 Purpose**
The purpose of this Software Requirements Specification (SRS) document is to define the functional, non-functional, and system requirements for **QuickKart**, an e-commerce platform similar to Flipkart. This platform will facilitate online shopping, allowing users to browse, search, and purchase products while enabling sellers to list and manage their inventory. An admin dashboard will allow administrators to moderate platform activities. Delivery logistics are entirely managed by third-party services.

### **1.2 Scope**
The QuickKart e-commerce platform aims to provide:  
- **User Features:** Product browsing, filtering, and searching; shopping cart; secure payments; order tracking.  
- **Seller Features:** Product listing, inventory management, and sales tracking.  
- **Admin Features:** User, product, and order moderation; platform analytics and reports.  

The platform will support web browsers and mobile devices, ensuring a seamless shopping experience. It will integrate secure payment gateways like **PayPal, Stripe, and UPI** for payment processing. Delivery and shipping services will be outsourced and managed by third-party providers. 

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
Delivery services are entirely managed by third-party logistics providers. QuickKart will coordinate with these services to ensure proper integration and order tracking.

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

- **Third-Party Delivery Integration**:  
  - APIs will be used to manage order shipping and delivery updates via third-party logistics providers.  
  - Users can track delivery statuses provided by external services.  

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
- Reliable communication with third-party delivery service APIs.  

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
- Tracking information will be updated in real-time using third-party logistics APIs.  

**6. Seller Dashboard**  
- Sellers can add, edit, and delete products.  
- Sellers can track orders and view product sales data.  

**7. Admin Panel**  
- Admins can manage users, sellers, products, and orders.  
- Admins can approve or reject seller product listings.  

**8. Delivery Integration**  
- Real-time updates for order shipping and delivery status provided by third-party services.  

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
- **Third-party Delivery APIs**: Use logistics provider APIs for shipping and delivery updates.  

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
![error case diagram](https://github.com/user-attachments/assets/809a8270-2230-4e79-8fc8-69df3adac8d7)

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
- Integration with third-party APIs like **Stripe, PayPal**, and delivery logistics services is required.  

---

## **8. System Architecture**

### **1. Frontend**
- **Technologies**: React.js (web), React Native (mobile).  
- **Role**: Provides user interactions and communicates with the backend via REST APIs.  

### **2. Backend**
- **Technologies**: Node.js, Express.js.  
- **Role**: Manages business logic and communicates with the database.  

### **3. Database**
- **Technology**: MySQL.  
- **Role**: Stores user, product, order, and seller data.  

### **4. Payment Gateway**
- **Technologies**: Stripe, PayPal, UPI.  
- **Role**: Secure payment processing.  

### **5. Delivery Service**
- **Integration**: Third-party delivery APIs.  
- **Role**: Manage shipping and provide real-time tracking for users.  

---
