# 🌱 AgriSense – Farm Management System

## 📌 Project Overview

AgriSense is a Django-based Farm Management Web Application designed to help farmers manage their agricultural activities and monitor financial performance through a centralized dashboard.

The application allows farmers to manage crop details, track agricultural expenses, record crop sales, and calculate overall profit or loss.

AgriSense aims to reduce manual record-keeping and help farmers make better decisions using organized digital records.

## 🎯 Problem Statement

Farmers often maintain crop details, investments, expenses, and sales using notebooks or spreadsheets. This makes it difficult to calculate actual profits, monitor crop performance, and manage multiple farming activities.

AgriSense provides a simple digital solution to organize farming operations and improve financial visibility.

## ✨ Key Features

### 1. Farmer Registration and Authentication
- Farmer registration and login.
- Secure authentication using Django.
- Individual farmer profiles.
- User-specific data access.

### 2. Crop Management
- Add, update, view, and delete crop details.
- Manage crop names and varieties.
- Record cultivated land in acres.
- Track farming seasons and start dates.
- Maintain harvest quantity and crop status.

### 3. Expense Tracking
- Record crop-related expenses.
- Categorize expenses such as seeds, fertilizers, pesticides, labour, irrigation, and transportation.
- Track individual crop investments.
- Calculate total expenses.

### 4. Sales Management
- Record crop sales.
- Store sale dates, quantities, and unit prices.
- Calculate total sales revenue.
- Validate sales to prevent selling more than the harvested quantity.

### 5. Dashboard and Profit Analysis
- View total active crops.
- Monitor total cultivated land.
- Track total investment.
- View total sales revenue.
- Calculate overall profit or loss.
- Monitor crop-wise financial performance.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Django | Web application framework |
| MySQL | Relational database |
| Django ORM | Database operations |
| HTML5 | Web page structure |
| CSS3 | Styling |
| Bootstrap 5 | Responsive user interface |
| JavaScript | Frontend interactions |

## 🏗️ Project Architecture

The application is organized into the following modules:

- **AgriSense:** Main Django project configuration and URL routing.
- **Accounts App:** User registration, login, logout, and farmer profile management.
- **Farm App:** Crop management, expense tracking, sales management, and dashboard functionality.
- **Templates:** HTML pages for the user interface.
- **Static Files:** CSS, JavaScript, and other frontend assets.

## 🗄️ Database Design

The application uses MySQL with Django ORM.

### Main Database Models

**1. FarmerProfile**
- User
- Mobile
- Village
- District
- State
- Total land acres

**2. Crop**
- Farmer
- Crop name
- Variety
- Acres
- Season
- Start date
- Harvested quantity
- Actual harvest date
- Status
- Notes

**3. CropExpense**
- Crop
- Expense date
- Category
- Amount
- Description
- Quantity

**4. CropSale**
- Crop
- Sale date
- Quantity sold
- Unit price

## 💰 Business Logic

AgriSense calculates crop profitability using the following formulas:

**Total Investment**

Total Investment = Sum of All Crop Expenses

**Total Sales Revenue**

Revenue = Quantity Sold × Unit Price

**Net Profit / Loss**

Net Profit = Total Sales Revenue − Total Investment

These calculations help farmers understand the financial performance of individual crops and their overall farming operations.

## ⚙️ Installation and Setup

### Prerequisites

- Python installed
- MySQL Server
- MySQL Workbench (optional)
- Git
- Visual Studio Code or PyCharm

### Step 1: Clone the Repository

```bash
git clone https://github.com/Akhil-2233/AgriSense.git
```

### Step 2: Navigate to the Project Directory

```bash
cd AgriSense
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

### Step 4: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 5: Configure MySQL Database

Create a MySQL database:

```sql
CREATE DATABASE agrisense;
```

Configure your MySQL database credentials in Django's `settings.py`.

Update the database engine to:

```python
'ENGINE': 'django.db.backends.mysql'
```

Configure the database name, username, password, host, and port according to your MySQL setup.

### Step 6: Apply Database Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

### Step 7: Run the Development Server

```bash
python manage.py runserver
```

### Step 8: Open the Application

Visit:

```text
http://127.0.0.1:8000/
```

## 🚀 Future Enhancements

- Weather forecasting integration.
- Crop yield prediction.
- Irrigation management.
- PDF report generation.
- Interactive charts and analytics.
- Multi-farm management.
- Mobile-friendly improvements.

## 🎓 Project Purpose

AgriSense was developed as a practical web development project to demonstrate full-stack development using Python and Django, relational database management using MySQL, CRUD operations, authentication, and business logic implementation.

## 👨‍💻 Developer

**Akhil**

GitHub: https://github.com/Akhil-2233

---

⭐ If you find this project useful, feel free to explore the repository!
