# 🍔 Food Delivery Application  

A **Spring Boot Application** built on **Microservices Architecture** that simulates an end-to-end food delivery system. It leverages **Spring Cloud components**, **Kafka**, and **JWT authentication** to ensure scalability, security, and seamless inter-service communication.  

---

## 🔑 Key Features  

- **Microservices Communication** → Interprocess communication between services.  
- **Service Discovery** → Centralized discovery using **Netflix Eureka Server**.  
- **API Gateway** → Routing and filtering with **Spring Cloud Gateway**.  
- **Secure Authentication** → All API requests are secured with **Spring Security + JWT tokens**.  
- **Event-Driven Architecture** → Real-time updates using **Apache Kafka**.  

---

## 🎯 Functionalities  

👤 **User Management**  
- Register as **Customer**, **Restaurant Owner**, **Delivery Agent**, or **Admin**.  
- Role-based access control for different functionalities.  

🍽️ **Restaurant & Menu Management**  
- Add new restaurants and food items.  
- Restaurant Owners can **update food items**.  
- Users can browse all available restaurants and their menus.  

🛒 **Order Management**  
- Place new orders.  
- Item quantity automatically updated upon order placement.  
- Order status updates trigger **notifications to restaurants** for preparation.  

💳 **Payment Management**  
- Users can make secure payments.  
- After successful payment:  
  - Order status is updated to **Confirmed**.  
  - A **notification is sent to Order Service**.  

---

## 🛠️ To Do  

- [ ] Implement **Delivery Service** (distance-based delivery, restaurant availability checks).  
- [ ] Add proper **error handling** with HTTP response codes.  
- [ ] Implement **Circuit Breaker** for fault tolerance.  
- [ ] Integrate **Micrometer/Prometheus** for monitoring and tracing.  
- [ ] Enhance **role-based authorization** for fine-grained security.  

---

## ⚙️ Microservices Overview  

### 🌐 Discovery Server  
- Hosts all microservices using **Eureka Server**.  

### 🚪 API Gateway  
- Runs on port **8080**.  
- Forwards requests from users to respective microservices.  
- Validates all requests via **Authorization Token**.  

### 🍴 Restaurant Service  
- Handles **restaurant and food item management**.  
- Restaurant Owners can add/update restaurants and their menus.  

### 📦 Order Service  
- Manages order lifecycle.  
- Verifies requests, updates inventory.  
- Notifies **Restaurant Service** after order confirmation.  

### 💰 Payment Service  
- Manages transactions.  
- Notifies **Order Service** after successful payment.  

---

✨ This project is a **hands-on demonstration** of building a **scalable, secure, and event-driven Food Delivery Application** using **Spring Boot & Microservices**.
