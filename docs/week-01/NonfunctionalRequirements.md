# Non-Functional Requirements Document
## Hotel Management System (HMS) with Casino & Gym Facilities
This document outlines the **non-functional requirements** for the **Hotel Management System** (HMS), including its scalability, availability, security, compliance, and performance expectations.

### **Scalability**
- **NFR-01:** The system shall be designed to handle up to **500 simultaneous users** (guests and staff) without any degradation in performance.
- **NFR-02:** The system shall be scalable to accommodate future growth, supporting up to **1000 users** without requiring major architectural changes.
- **NFR-03:** The system’s architecture must support **horizontal scaling** (adding more servers) to ensure efficient handling of increasing traffic during peak periods (e.g., holidays, special events).

### **Availability**
- **NFR-04:** The system must ensure **99.9% uptime**, which is approximately **8 hours of downtime** per year. This includes both planned maintenance and unplanned outages.
- **NFR-05:** Maintenance windows must be scheduled during **off-peak hours**, and administrators must notify users at least 24 hours in advance of any scheduled downtime.

### **Data Backup & Recovery**
- **NFR-06:** The system must perform **automated backups** of all critical data (e.g., guest records, financial transactions, bookings) every **6 hours**.
- **NFR-07:** The system shall support **data recovery** with a **recovery time objective (RTO)** of **1 hour** in the event of a failure. Data must be recoverable from the most recent backup.
- **NFR-08:** Backups must be stored securely in **encrypted formats** and must be retrievable only by authorized personnel.
- **NFR-09:** The system shall support **manual backups** prior to major updates or system changes.

### **Role-Based Access Control (RBAC)**
- **NFR-10:** The system shall implement **role-based access control (RBAC)** to ensure that users can only access features and data relevant to their role. For example, receptionists, hotel managers, casino staff, and guests must each have different levels of access.
- **NFR-11:** The system must provide an **admin interface** for creating, updating, and removing user roles.
- **NFR-12:** Access to sensitive data and functions (e.g., financial information, guest personal details) must be restricted to specific roles, with **audit logging** for all changes in roles and permissions.
  
### **Audit Logging**
- **NFR-13:** The system must **log** all financial transactions, check-ins, room bookings, and other critical activities for **security audits** and **regulatory compliance**.
- **NFR-14:** All system logs should be protected against tampering and stored in a secure location. Logs must be retained for a minimum of **2 years** for regulatory review.
- **NFR-15:** The system should have the capability to filter and query logs based on date, user, activity, or transaction type to assist with audits.

### **Employee Activity Tracking**
- **NFR-16:** The system shall **log and track all employee activities**, including login/logout, modifications to bookings, processing of payments, and system access to sensitive data.
- **NFR-17:** Any **suspicious or unauthorized actions** by employees (e.g., accessing guest financial data) should trigger **automated alerts** to the administrator.

### **Configurable Policies**
- **NFR-18:** The system should allow for **customizable policy templates**, allowing administrators to apply different rules across hotel, casino, and gym facilities.

### **Response Time**
- **NFR-19:** The system must process room booking requests, casino bets, and gym registrations in **less than 3 seconds** per transaction under normal load conditions.
- **NFR-20:** All user interactions, including guest check-in/check-out, transaction processing, and room service requests, must be completed with minimal delays (within 2 seconds) to enhance the user experience.

### **Cross-Platform Compatibility**
- **NFR-21:** The system must support all major desktop operating systems, including **Windows** and **macOS**.
- **NFR-22:** The system must also be accessible from **mobile devices** (iOS and Android) with an optimized user interface for **small screens** and **touch interfaces**.
- **NFR-23:** The user interface must be **responsive**, adjusting seamlessly to different screen sizes and device types without any loss of functionality.

### **User-Friendly Interface**
- **NFR-24:** The system’s interface must be **intuitive and easy to use**, requiring no more than **1 hour of training** for new employees to perform basic operations.
- **NFR-25:** The user interface should incorporate **best practices in UX design**, ensuring users can efficiently navigate through the system without extensive guidance.
- **NFR-26:** The system must be designed for **accessibility**, with settings like high contrast, text-to-speech, and alternative text for images.

### **System Performance**
- **NFR-27:** The system must be capable of handling **up to 1000 database transactions per minute** without slowdowns or system crashes.
- **NFR-28:** The database should be optimized to ensure fast query execution, especially during high-traffic periods (e.g., check-in/check-out times).
- **NFR-29:** Load testing must be conducted regularly to simulate peak usage and ensure the system meets performance benchmarks.

### **Integration with Payment Gateways**
- **NFR-30:** The system must support multiple **payment methods**, including **credit/debit cards**, **mobile payments** (e.g., Apple Pay, Google Pay), and **digital wallets** (e.g., PayPal).
- **NFR-31:** Payment transactions must be processed in **real-time**, with a response time of **less than 3 seconds** to ensure smooth guest experience.
- **NFR-32:** The payment gateway must be compliant with **PCI DSS** standards to ensure secure handling of payment information.

### **Automated Alerts & Notifications**
- **NFR-33:** The system must send **email/SMS notifications** for important events such as bookings, cancellations, payment confirmations, and loyalty rewards.
- **NFR-34:** The system must allow for **customizable notifications** based on user preferences, including event reminders and special offers.
- **NFR-35:** Notifications should be triggered in **real-time** to provide immediate updates to guests and staff.

### **Multi-Language Support**
- **NFR-36:** The system shall support **English**, **Spanish**, **Italian**, **French**, and **Albanian** as the minimum languages for international guests.
- **NFR-37:** The language settings should be **easily configurable** by the user, allowing them to select their preferred language upon initial login or through their profile settings.
- **NFR-38:** All system labels, buttons, forms, and notifications must be accurately translated into the supported languages, maintaining proper formatting.

### **Customizable Reports**
- **NFR-39:** The system must allow **hotel administrators** to generate **custom reports** based on configurable filters such as **date range**, **revenue**, and **occupancy rates**.
- **NFR-40:** Reports must be exportable in formats including **PDF**, **CSV**, and **Excel**, to enable further analysis.
- **NFR-41:** Report generation should be **fast**, with a response time of **less than 5 seconds** even for large datasets.

### **Guest Self-Service Portal**
- **NFR-42:** The system must provide a **self-service portal** where guests can manage their bookings, check in/check out, upgrade rooms, and view/manage their casino and gym memberships.
- **NFR-43:** The guest portal must be available **24/7** and be **responsive**, ensuring it functions seamlessly across desktop, tablet, and mobile devices.
- **NFR-44:** The portal should provide **real-time updates** for booking modifications, cancellations, and payment confirmations.

### **Security & Data Protection**
- **NFR-45:** The system must comply with **GDPR** (General Data Protection Regulation) for guests in Europe and **CCPA** (California Consumer Privacy Act) for guests in California to ensure guest data privacy and protection.
- **NFR-46:** All personal and sensitive data (e.g., credit card numbers, ID details) must be **encrypted** both in transit (using TLS/SSL) and at rest (using AES encryption).
- **NFR-47:** The system should support **data anonymization** and **user consent management** for collecting and processing personal information.

### **Age Verification for Casino**
- **NFR-48:** The system must verify the **age** of guests (18+ or 21+) before allowing access to casino features. Verification should be done using **government-issued IDs** (e.g., driver’s license, passport).
- **NFR-49:** Age verification must be performed in **real-time** and prevent unauthorized users from participating in gambling activities.

### **Compliance with Gambling Regulations**
- **NFR-50:** The casino module must comply with **local and international gambling regulations**.
- **NFR-51:** The system must allow **casino managers** to configure and enforce gambling policies, including **betting limits** and responsible gaming features.

### **Legal Compliance for Hotel Check-Ins**
- **NFR-52:** The system must require **ID verification** during the hotel check-in process to comply with **local hospitality regulations**.
- **NFR-53:** The system should securely store guest ID information for **regulatory audits** and maintain compliance with relevant laws.

### **Tax & Financial Compliance**
- **NFR-54:** The system must generate **automated tax reports** based on regional tax regulations for both the hotel, casino, and gym.
- **NFR-55:** All **financial transactions** must be categorized and stored in compliance with **regional tax laws**, and the system must support the generation of tax reports on demand.

### **Third-Party API Integration**
- **NFR-56:** The system must support integration with **third-party hotel listing platforms** (e.g., Booking.com, Expedia) to update room availability and handle bookings.
- **NFR-57:** The system must support integration with third-party **casino software** providers for payment processing and guest activity tracking.
- **NFR-58:** The system must allow integration with third-party **gym membership** platforms for unified user management.

