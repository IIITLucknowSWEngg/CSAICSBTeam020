
# System Context Diagram

```plantuml
@startuml

' External Actors
actor "Customer (User)" as Customer
actor "Seller (Vendor)" as Seller
actor "Admin" as Admin
actor "Payment Gateway" as PaymentGateway
actor "Shipping Service" as ShippingService
actor "Notification Service" as NotificationService
actor "Customer Support" as CustomerSupport

' System Boundary: Flipkart Clone
package "Flipkart Clone" {

    ' Subsystems
    rectangle "User Registration \nand Authentication" as Registration
    rectangle "Product Catalog \nand Management" as ProductCatalog
    rectangle "Order Management" as OrderManagement
    rectangle "Payment Integration" as Payment
    rectangle "Ratings and Reviews" as Ratings
    rectangle "Admin Panel" as AdminPanel
    rectangle "Push Notifications" as PushNotifications
    rectangle "In-App Chat \nand Support" as ChatSupport
    rectangle "Real-Time Shipping Tracking" as ShippingTracking
    rectangle "Customer Support" as Support
}

' Relationships between actors and system components
Customer --> Registration : Sign Up/Login
Customer --> ProductCatalog : Browse Products
Customer --> OrderManagement : Place Order
Customer --> Payment : Process Payment
Customer --> Ratings : Rate Product
Customer --> PushNotifications : Receive Notifications
Customer --> ChatSupport : Contact Support

Seller --> Registration : Register/Login
Seller --> ProductCatalog : Manage Products
Seller --> OrderManagement : Manage Orders
Seller --> PushNotifications : Receive Notifications

Admin --> AdminPanel : Manage Users/Sellers/Orders
Admin --> ProductCatalog : Manage Products
Admin --> OrderManagement : Monitor Orders
Admin --> Payment : Monitor Payments
Admin --> PushNotifications : Send Notifications
Admin --> Ratings : Manage Reviews

' External Interactions
Payment --> PaymentGateway : Process Payment Transactions
ShippingTracking --> ShippingService : Track Shipments
PushNotifications --> NotificationService : Send Notifications
Support --> CustomerSupport : Handle Customer Issues

@enduml
```

# Container Diagram

## Customer Code

```plantuml
@startuml
!define RECTANGLE rectangle

title Container Diagram - Flipkart Clone (Customer)

' Primary containers
RECTANGLE "Customer Mobile App" as customerApp <<Mobile Application>> #lightblue
RECTANGLE "Customer API Gateway" as customerGateway <<API Gateway>> #lightblue

' Database containers
RECTANGLE "Product Database" as productDB <<Database>> #lightyellow
RECTANGLE "User Database" as userDB <<Database>> #lightyellow
RECTANGLE "Order Database" as orderDB <<Database>> #lightyellow

' External systems
RECTANGLE "External Payment System" as paymentSystem <<External System>> #pink
RECTANGLE "Shipping Service" as shippingService <<External System>> #pink
RECTANGLE "Push Notification Service" as pushNotification <<External System>> #pink

' Relationships between containers
customerApp --> customerGateway : "API Calls"
customerGateway --> productDB : "Manage Product Data"
customerGateway --> userDB : "Manage User Data"
customerGateway --> orderDB : "Manage Orders"
customerGateway --> paymentSystem : "Process Payments"
customerGateway --> shippingService : "Track Orders"
customerGateway --> pushNotification : "Receive Notifications"

@enduml
```

## Seller Code

```plantuml
@startuml
!define RECTANGLE rectangle

title Container Diagram - Flipkart Clone (Seller)

' Primary containers
RECTANGLE "Seller Mobile App" as sellerApp <<Mobile Application>> #lightgreen
RECTANGLE "Seller API Gateway" as sellerGateway <<API Gateway>> #lightgreen

' Database containers
RECTANGLE "Product Database" as productDB <<Database>> #lightyellow
RECTANGLE "Order Database" as orderDB <<Database>> #lightyellow

' External systems
RECTANGLE "External Payment System" as paymentSystem <<External System>> #pink
RECTANGLE "Push Notification Service" as pushNotification <<External System>> #pink

' Relationships between containers
sellerApp --> sellerGateway : "API Calls"
sellerGateway --> productDB : "Manage Product Data"
sellerGateway --> orderDB : "Manage Orders"
sellerGateway --> paymentSystem : "Process Payments"
sellerGateway --> pushNotification : "Receive Notifications"

@enduml
```

## Admin Code

```plantuml
@startuml
!define RECTANGLE rectangle

title Container Diagram - Flipkart Clone (Admin)

' Primary containers
RECTANGLE "Admin Web Dashboard" as adminPortal <<Web Application>> #lightcoral
RECTANGLE "Admin API Gateway" as adminGateway <<API Gateway>> #lightcoral

' Database containers
RECTANGLE "Product Database" as productDB <<Database>> #lightyellow
RECTANGLE "User Database" as userDB <<Database>> #lightyellow
RECTANGLE "Order Database" as orderDB <<Database>> #lightyellow

' External systems
RECTANGLE "Push Notification Service" as pushNotification <<External System>> #pink

' Relationships between containers
adminPortal --> adminGateway : "API Calls"
adminGateway --> productDB : "Manage Product Data"
adminGateway --> userDB : "Manage User/Seller Data"
adminGateway --> orderDB : "Monitor Orders"
adminGateway --> pushNotification : "Send Notifications"

@enduml
```

# Component Diagram

## Customer Code

```plantuml
@startuml
' External Actors
actor "Customer" as Customer
actor "Admin" as Admin
actor "Payment Gateway" as PaymentGateway
actor "Shipping Service" as ShippingService
actor "Notification Service" as NotificationService
actor "Customer Support" as CustomerSupport

' System Boundary: Flipkart Clone
package "Flipkart Clone" {

    ' Subsystems specifically related to Customer
    rectangle "User Registration \nand Authentication" as UserRegistration
    rectangle "Product Catalog \nand Management" as ProductCatalog
    rectangle "Order Management" as OrderManagement
    rectangle "Payment Processing" as PaymentProcessing
    rectangle "Ratings and Reviews" as Ratings
    rectangle "Push Notifications" as PushNotifications
    rectangle "In-App Chat \nand Support" as ChatSupport
    rectangle "Real-Time Shipping Tracking" as ShippingTracking
}

' Relationships between Customer and system components
Customer --> UserRegistration : Sign Up/Login
Customer --> ProductCatalog : Browse Products
Customer --> OrderManagement : Place Order
Customer --> PaymentProcessing : Process Payment
Customer --> Ratings : Rate Product
Customer --> PushNotifications : Receive Notifications
Customer --> ChatSupport : Contact Support

' External Interactions
PaymentProcessing --> PaymentGateway : Process Payment Transactions
ShippingTracking --> ShippingService : Track Shipments
PushNotifications --> NotificationService : Send Notifications
ChatSupport --> CustomerSupport : Handle Customer Issues

@enduml
```

# Deployment Diagram

```plantuml
@startuml
title Deployment Diagram - Flipkart Clone System

node "Customer's Mobile Device" {
    [Customer Mobile App] <<Mobile App>>
}

node "Seller's Mobile Device" {
    [Seller Mobile App] <<Mobile App>>
}

node "Admin's PC" {
    [Admin Web Dashboard] <<Web App>>
}

node "Web Server" {
    [Order Management Service] <<Microservice>>
    [Payment Service] <<Microservice>>
    [User Management Service] <<Microservice>>
    [Product Catalog Service] <<Microservice>>
}

node "Database Server" {
    database "Product Database" as ProductDB
    database "User Database" as UserDB
    database "Order Database" as OrderDB
}

cloud "Third-Party Services" {
    [Payment Gateway] <<External Service>>
    [Shipping Service] <<External Service>>
}

' Connections
[Customer Mobile App] --> [Order Management Service] : "Place Order"
[Customer Mobile App] --> [Payment Service] : "Process Payment"
[Customer Mobile App] --> [Product Catalog Service] : "Browse Products"
[Customer Mobile App] --> [User Management Service] : "Manage Profile"

[Seller Mobile App] --> [Product Catalog Service] : "Manage Products"
[Seller Mobile App] --> [Order Management Service] : "Manage Orders"
[Seller Mobile App] --> [Payment Service] : "View Earnings"

[Admin Web Dashboard] --> [Product Catalog Service] : "Manage Products"
[Admin Web Dashboard] --> [Order Management Service] : "Monitor Orders"
[Admin Web Dashboard] --> [User Management Service] : "Manage Users"

[Order Management Service] --> ProductDB : "Manage Product Data"
[Payment Service] --> ProductDB : "Access Product Info"
[Payment Service] --> OrderDB : "Manage Order Data"
[User Management Service] --> UserDB : "Manage User Data"

[Payment Service] --> [Payment Gateway] : "Process Payment"
[Order Management Service] --> [Shipping Service] : "Track Orders"

@enduml
