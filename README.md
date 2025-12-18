# TASK S2.03 DATA STRUCTURE MONGODB
---
# 🕶️  Optica Store

This repository contains a **MongoDB-based data modeling exercise** focused on designing and implementing a real-world database for an optical store called **“Cul d'Ampolla”**.

The main goal of this project is to **translate a relational (SQL) data model into a NoSQL (MongoDB) solution**, understanding how document-based databases handle relationships, embedded data, and references.

---

## 🚀 Skills & Concepts Learned

By completing these exercises, you will practice and reinforce the following skills:

- Designing a **NoSQL data model** from functional requirements  
- Translating **SQL concepts (tables, foreign keys, joins)** into **MongoDB documents and references**  
- Choosing between **embedded documents vs referenced documents**  
- Working with **ObjectId references** instead of numeric IDs  
- Managing **one-to-one and one-to-many relationships** in MongoDB  
- Using **MongoDB Compass** for visual database management  
- Running MongoDB in a **Docker container** using Docker Compose  
- Exporting and sharing MongoDB schemas and collections  
- Structuring a project for academic and collaborative environments  

---

## 📘 Project Description

An optical store named **“Cul d'Ampolla”** wants to computerize the management of its **customers, suppliers, glasses, employees, and sales**.

The system must store and relate the following information:

---

### 🏭 Suppliers
For each supplier, the system stores:
- Name  
- Full postal address (street, number, floor, door, city, ZIP code, country)  
- Phone number  
- Fax  
- NIF (tax identification number)

---

### 👓 Glasses
For each pair of glasses:
- Brand  
- Graduation for each lens (left and right)  
- Frame type (**floating, plastic, or metal**)  
- Frame color  
- Lens color (left and right)  
- Price  
- Supplier reference (which supplier provides the glasses)

---

### 👤 Customers
For each customer:
- Full name  
- Postal address  
- Phone number  
- Email address  
- Registration date  
- Reference to another customer who recommended them (if applicable)

---

### 🧑‍💼 Employees & Sales
- Each sale records:
  - The customer who bought the glasses  
  - The employee who made the sale  
  - The glasses sold  
  - The exact date and time of the sale  

This allows tracking **who sold what, to whom, and when**.

---

## 🗂️ Database Design Approach

- Each main entity is modeled as a **MongoDB collection**:
  - `customer`
  - `supplier`
  - `glasses`
  - `employee`
  - `sale`
- Relationships are handled using **ObjectId references** instead of foreign keys.
- Complex attributes such as addresses are modeled as **embedded documents**.
- Sales are modeled as a separate collection to maintain a clean and scalable structure.

---

## 🧪 Tools & Technologies Used

- **MongoDB** – NoSQL document database  
- **MongoDB Compass** – Visual GUI for managing collections and documents  
- **Docker** – Containerization of the MongoDB environment  
- **Docker Compose** – Service orchestration and easy project setup  
- **mongosh** – MongoDB shell for direct database interaction  
- **Git & GitHub** – Version control and project sharing  

---

## 🛠️ Installation
Clone this repository:  
git clone https://github.com/cristhianchulca49/S2.03.mongoDB-estructura

---

## 📦 Project Setup

The project includes:
- A `docker-compose.yml` file to easily start MongoDB  
- JSON/JS files defining collections and schemas  
- Example documents for each collection  

To start the database locally:
```docker compose up -d```

---

## 🤝 Contributions are welcome! 
- Please follow these steps to contribute: 
- Fork the repository Create a new branch: git checkout -b feature/NewFeature 
- Make your changes and commit them: git commit -m 'Add New Feature' 
- Push the changes to your branch: git push origin feature/NewFeature 
- Open a Pull Request
