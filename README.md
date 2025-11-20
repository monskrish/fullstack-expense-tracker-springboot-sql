# 📘 Full Stack Expense Tracker

### JavaFX • Spring Boot • MySQL • REST API

A complete full-stack **Expense Tracker** application built using **Java**, **JavaFX**, **Spring Boot**, and **MySQL**.
This project helps users manage their personal finances with a clean desktop UI and a powerful backend API.

---

## 🚀 Features

### 🔐 **User Authentication**

* User login & signup
* Basic validation and credential handling

### 💰 **Transaction Management**

* Add, update, and delete income/expense records
* Optional category assignment (nullable FK)
* Stores precise currency values using `DECIMAL(10,2)`

### 🗂️ **Category Management**

* Create, edit, delete categories
* Color-coded categories for easy identification
* Fully synced with each user

### 📊 **Financial Insights**

* Monthly and yearly summaries
* Total income / total expense / net balance
* Bar chart visualization (Income vs Expense)

### 📅 **Filtering & Pagination**

* View transactions by year or year+month
* Recent transactions API with page-size control

### 🎨 **Clean JavaFX UI**

* Built using MVC pattern
* Reusable components (`CategoryComponent`, `TransactionComponent`)
* Smooth navigation with a custom `ViewNavigator`
* Loading animation pane for better UX

---

## 🏗️ Architecture

### 🖥️ **Front-End (JavaFX)**

* Follows **MVC architecture**
* JavaFX programmatic UI (no FXML)
* Uses `Gson` for JSON serialization
* Communicates with backend using custom HTTP utility classes

### ⚙️ **Back-End (Spring Boot)**

* **Layered Architecture:**
  `Controller → Service → Repository → MySQL`
* RESTful API design with `/api/v1` base path
* Business logic handled at Service level
* Spring Data JPA for database operations
* Dependency Injection using `@Autowired`

### 🗄️ **Database (MySQL)**

Normalized schema with 3 main tables:

1. **user**
2. **transaction_category**
3. **transaction**

Includes foreign keys, proper indexing, and date-based filtering.

---

## 📚 Tech Stack

| Area           | Technologies          |
| -------------- | --------------------- |
| **Frontend**   | JavaFX                |
| **Backend**    | Spring Boot (3.3+)    |
| **Language**   | Java 24               |
| **Database**   | MySQL 8+              |
| **Build Tool** | Maven                 |
| **Libraries**  | Gson, Spring Data JPA |

---

## 🧩 API Endpoints (Summary)

### 🔑 User

* `POST /api/v1/user/login`
* `POST /api/v1/user`

### 🗂️ Categories

* `POST /api/v1/transaction-category`
* `GET /user/{userId}`
* `PUT /{id}`
* `DELETE /{id}`

### 💵 Transactions

* `POST /api/v1/transaction`
* `PUT /api/v1/transaction`
* `DELETE /{id}`
* `GET /recent/user/{id}`
* `GET /user/{id}?year=&month=`
* `GET /years/{id}`

---

## 🧪 Screenshots (Add later)

You can add screenshots here once you upload images.

```
![Dashboard Screenshot](screenshots/dashboard.png)
![Chart Screenshot](screenshots/chart.png)
```

---

## ▶️ How to Run

### **Backend**

```bash
cd backend
mvn spring-boot:run
```

### **Frontend**

```bash
cd frontend
mvn clean install
mvn javafx:run
```

---

## 💡 Future Improvements

* JWT-based authentication
* Export reports to Excel/PDF
* Dark/Light theme support
* Deployment to cloud

