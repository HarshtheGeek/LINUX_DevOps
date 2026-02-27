# LINUX_DevOps

## 1) How Does the Internet Work?

At a high level, the internet is a global network of interconnected computers that communicate using standardized protocols.

### Core Components

**1. Client**

* Your device (browser, mobile app).
* Initiates requests.

**2. Server**

* A machine that responds to client requests.

**3. IP Address**

* Unique address of a device on a network.
* Example: `142.250.183.14`

**4. DNS (Domain Name System)**

* Converts domain names (e.g., google.com) → IP addresses.
* Like a phonebook for the internet.

**5. Protocols**

* HTTP/HTTPS → Web communication
* TCP → Reliable data transfer
* UDP → Faster, less reliable transfer
* SSL/TLS → Encryption

---

### Step-by-Step Flow (When You Open a Website)

1. You type `example.com` in the browser.
2. DNS resolves it to an IP address.
3. Browser sends an HTTP request to that IP.
4. Server processes the request.
5. Server sends back a response (HTML/CSS/JS).
6. Browser renders the page.

This is called the **request-response cycle**.

---

## 2) What is a Server?

A server is a machine (physical or virtual) that provides services to other machines.

### Types of Servers

* Web Server
* Application Server
* Database Server
* File Server
* Mail Server

### Important:

A server is not defined by hardware — it is defined by **role**.

Example:

* Your laptop can act as a server if it hosts an API.

---

## 3) Difference Between Web Server and Application Server

| Feature        | Web Server           | Application Server     |
| -------------- | -------------------- | ---------------------- |
| Main Role      | Serve static content | Execute business logic |
| Content        | HTML, CSS, images    | Dynamic responses      |
| Examples       | Nginx, Apache        | Node.js, Spring Boot   |
| Speed          | Very fast            | Slightly heavier       |
| Logic Handling | Minimal              | Full business logic    |

### Flow in Real Architecture

Client → Web Server → Application Server → Database

Example:

* Nginx (web server) handles static files.
* Node.js (application server) handles API logic.

---

## 4) Types of Applications

### 1. Standalone Applications

* Run on a single machine.
* No internet required.
* Example: MS Word.

### 2. Web Applications

* Accessed via browser.
* Hosted on remote server.
* Example: Gmail.

### 3. Mobile Applications

* Installed on mobile devices.
* Can be native or hybrid.
* Example: WhatsApp.

### 4. Distributed Applications

* Components spread across multiple servers.
* Example: Microservices architecture.

---

## 5) What are Standalone Apps?

Applications that:

* Run locally.
* Do not require server interaction.
* Store data locally.

Examples:

* VLC
* Calculator
* Offline IDE

### Architecture

User → App → Local OS → Local Storage

No network dependency.

---

## 6) What are Web Applications?

Applications hosted on a server and accessed through browsers.

### Characteristics

* Client-Server architecture
* Centralized data
* Scalable
* Requires internet

### Architecture

Browser (Frontend)
↓
Web Server
↓
Application Server
↓
Database

Examples:

* Amazon
* LinkedIn
* GitHub

---

## 7) What is Application Support?

Application support refers to maintaining and monitoring live applications to ensure smooth operation.

### Responsibilities

* Monitoring logs
* Fixing bugs
* Restarting services
* Handling production issues
* Performance optimization

### Tools Used

* Linux commands (top, ps, netstat)
* Monitoring tools (Prometheus)
* Log tools (ELK Stack)

This is operational maintenance of a running system.

---

## 8) What is Application Maintenance?

Maintenance focuses on long-term improvement and sustainability.

### Types

1. Corrective Maintenance
   Fixing defects.

2. Adaptive Maintenance
   Updating due to OS/library changes.

3. Perfective Maintenance
   Adding enhancements.

4. Preventive Maintenance
   Refactoring for future stability.

---

## DevOps Perspective

* Internet → Communication layer
* Server → Hosting layer
* Web/App Server → Execution layer
* Support → Operational layer
* Maintenance → Lifecycle layer

These form the foundation of infrastructure engineering.


Tell me your goal (DevOps job / interviews / project clarity).

