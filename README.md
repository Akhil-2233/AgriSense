# 🌱 AgriSense – Farm Management System

**AgriSense** is a Django-based farm management web application designed to help farmers manage crops, track agricultural expenses, record sales, and monitor profits or losses through a simple and user-friendly dashboard.

The project aims to reduce manual record-keeping and help farmers make better decisions using organized agricultural and financial information.

## 📌 Project Overview

Farmers often maintain crop details, investments, expenses, and sales using notebooks or spreadsheets. This makes it difficult to calculate profits and compare crop performance.

AgriSense provides a centralized digital platform where farmers can manage their farming activities and monitor financial performance efficiently.

## 🎯 Objectives

- Digitize agricultural record management.
- Simplify crop and expense tracking.
- Maintain crop-wise sales information.
- Calculate total investment and revenue.
- Monitor crop-wise and overall profitability.
- Help farmers make informed decisions.

## ✨ Features

### 1. Farmer Registration and Authentication
- User registration and login.
- Secure authentication using Django.
- Individual farmer profiles.
- Farmer contact and land information.

### 2. Crop Management
- Add, edit, view, and delete crop records.
- Maintain crop names and varieties.
- Track land area in acres.
- Manage farming seasons and start dates.
- Record harvest quantity and crop status.

### 3. Expense Tracking
- Record expenses for individual crops.
- Categorize agricultural expenses:
  - Seeds
  - Fertilizers
  - Pesticides
  - Labour
  - Irrigation
  - Tractor and ploughing
  - Equipment rental
  - Transportation
  - Harvesting
  - Other expenses
- Calculate total crop investment.

### 4. Sales Management
- Record crop sales.
- Maintain sale dates and quantities.
- Store unit prices.
- Calculate sales revenue.
- Validate sales quantities against harvested output.

### 5. Dashboard and Profit Calculation
- Display total active crops.
- Monitor total cultivated land.
- View total investment.
- Track total sales revenue.
- Calculate overall profit or loss.
- View crop-wise financial performance.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Python | Backend programming |
| Django | Web framework |
| SQLite | Database |
| Django ORM | Database operations |
| HTML5 | Web page structure |
| CSS3 | Styling |
| Bootstrap 5 | Responsive user interface |
| JavaScript | Frontend interactions |

## 🏗️ Project Architecture

```text
AgriSense/
│
├── AgriSense/
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
│
├── accounts/
│   ├── migrations/
│   ├── templates/
│   ├── models.py
│   ├── views.py
│   └── urls.py
│
├── farm/
│   ├── migrations/
│   ├── models.py
│   ├── views.py
│   └── urls.py
│
├── templates/
│
├── static/
│
├── manage.py
├── requirements.txt
└── README.md
```

*Note: This is a representative structure. Actual files may vary depending on the project implementation.*

## 🗄️ Database Models

The application uses relational database models.

**FarmerProfile**
- User
- Mobile
- Village
- District
- State
- Total land acres

**Crop**
- Farmer
- Crop name
- Variety
- Acres
- Season
- Start date
- Harvested quantity
- Status
- Notes

**CropExpense**
- Crop
- Expense date
- Category
- Amount
- Description
- Quantity

**CropSale**
- Crop
- Sale date
- Quantity sold
- Unit price

## 💰 Business Logic

AgriSense uses simple financial calculations to monitor agricultural profitability.

**Total Investment**

```python
Total Investment = Sum of All Crop Expenses
```

**Total Sales Revenue**

```python
Revenue = Quantity Sold * Unit Price
```

**Net Profit or Loss**

```python
Net Profit = Total Sales Revenue - Total Investment
```

The application also validates sales to prevent the quantity sold from exceeding the harvested quantity.

## ⚙️ Installation and Setup

Follow these steps to run the project locally.

### Step 1: Clone the Repository

```bash
git clone https://github.com/Akhil-2233/AgriSense.git
```

### Step 2: Navigate to the Project Folder

```bash
cd AgriSense
```

### Step 3: Create a Virtual Environment

```bash
python -m venv venv
```

### Step 4: Activate the Virtual Environment

For Windows:

```bash
venv\Scripts\activate
```

### Step 5: Install Dependencies

```bash
pip install -r requirements.txt
```

### Step 6: Apply Database Migrations

```bash
python manage.py migrate
```

### Step 7: Create an Admin Account (Optional)

```bash
python manage.py createsuperuser
```

### Step 8: Run the Development Server

```bash
python manage.py runserver
```

Open your browser and visit:

```text
http://127.0.0.1:8000/
```

## 🔐 Security and Access Control

- Django authentication for user login and logout.
- Login-required restrictions for protected pages.
- User-specific data filtering.
- Validation of crop sales against harvested quantities.

## 🚀 Future Enhancements

- Weather forecasting integration.
- Crop yield prediction using machine learning.
- Irrigation management.
- Multi-farm management.
- PDF report generation.
- Interactive charts and analytics.
- Export and import of farm records.

## 💡 Project Impact

AgriSense helps farmers:
- Reduce manual paperwork.
- Track agricultural investments.
- Understand crop profitability.
- Identify high-expense activities.
- Compare crop performance.
- Improve farming decisions.

## 👨‍💻 Developer

**Akhil**

GitHub: [Akhil-2233](https://github.com/Akhil-2233)

Project Repository: [AgriSense](https://github.com/Akhil-2233/AgriSense)

---

⭐ If you find this project useful, consider giving the repository a star!

**AgriSense – Smart Farming, Better Decisions.** 🌱
