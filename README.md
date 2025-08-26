# Expense Tracking System  

## 📑 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Setup Instructions](#setup-instructions)
- [Database Setup](#database-setup)
- [How It Works](#how-it-works)
- [Architecture Diagram](#architecture-diagram)
- [Project Screenshots](#project-screenshots)
- [Project Live Demo](#project-live-demo)
- [Let's Connect](#lets-connect)

## Project Overview

A full-stack **Expense Tracking System** built with **Streamlit (frontend)** and **FastAPI (backend)**.  
This project helps users efficiently **track, update, and analyze expenses** with a simple interface.

## Features  
- **Add & Update Expenses**  
- **Analytics by Expense Category** (e.g., Food, Rent, etc.)  
- **Monthly Expense Analytics**  
- **Fast & Scalable Backend API (FastAPI + MySQL)**  
- **Test Coverage with Pytest**  

## Tech Stack  
- **Frontend:** Streamlit  
- **Backend:** FastAPI with Uvicorn  
- **Database:** MySQL  
- **Testing:** Pytest  
- **Language:** Python 3.13.5

## Project Structure
 
  - `frontend/` – Contains Streamlit frontend code  
  - `backend/` – Contains FastAPI backend server code  
  - `tests/` – Contains Pytest test cases for frontend and backend  
  - `requirements.txt` – Lists required Python dependencies  
  - `README.md` – Includes project documentation and overview  

## Setup Instructions  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/bilalayub10/Python_Expense_Tracking_System.git
   cd Python_Expense_Tracking_System

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt

3. **Set up database credentials** (see **Database Setup** section below)


4. **Run the FastAPI server**
   ```bash
   uvicorn backend.server:app --reload

5. **Run the Streamlit app**
   ```bash
   streamlit run frontend/app.py

6. **Run tests** (optional)
   ```bash
   pytest tests/

## Database Setup

This project uses a **MySQL database**. The schema includes an `expenses` table with the following columns:

| Column         | Type         | Description                 |
|----------------|--------------|-----------------------------|
| `id`           | INT          | Primary Key, Auto Increment |
| `expense_date` | DATE         | Date of the expense         |
| `amount`       | FLOAT        | Expense amount              |
| `category`     | VARCHAR(255) | Expense category            |
| `notes`        | TEXT         | Description of the expense  |


### Option 1: Import an Existing `.sql` File

If you already have an `.sql` file with the above schema, you can import it into **MySQL Workbench** or any other MySQL client.

### Option 2: Create Your Own Schema

Manually create the table using the schema and insert sample data for testing:

```sql
CREATE TABLE expenses (
    id INT PRIMARY KEY AUTO_INCREMENT,
    expense_date DATE,
    amount FLOAT,
    category VARCHAR(255),
    notes TEXT
);
```
### Database Credentials Setup

The backend connects to MySQL using credentials stored in a .env file for security.

1. Create a `.env` file in the project root:

```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=yourpassword
DB_NAME=expenses_db
```

2. Ensure `.env` is not committed to GitHub (already added in .gitignore).

3. The backend will automatically read these values when establishing the database connection.

## How It Works

The system follows a simple full-stack flow:

1. **User** interacts with the **Streamlit app** (frontend).
2. The frontend sends requests to the **FastAPI backend**.
3. The backend connects with the **MySQL database** to fetch or update expenses.
4. The response is returned to Streamlit, where users see **analytics and visualizations**.

## Architecture Diagram

```sql
+-----------+        +-----------+        +-----------+
|   User    | <----> | Streamlit | <----> |  FastAPI  |
+-----------+        +-----------+        +-----------+
                                       |
                                       v
                                 +-----------+
                                 |   MySQL   |
                                 +-----------+
```

## Project Screenshots

<p align="center">
  <img src="https://github.com/bilalayub10/Python_Expense_Tracking_System/blob/main/Images/Add_Update%20Tab.JPG?raw=true" alt="Add_Update Tab">
</p>
<p align="center"><b>Figure:</b> Add/Update Tab</p>

<p align="center">
  <img src="https://github.com/bilalayub10/Python_Expense_Tracking_System/blob/main/Images/Analytics%20By%20Category%20Tab.gif?raw=true" alt="Analytics By Category Tab">
</p>
<p align="center"><b>Figure:</b> Analytics By Category Tab</p>

<p align="center">
  <img src="https://github.com/bilalayub10/Python_Expense_Tracking_System/blob/main/Images/Analytics%20By%20Months%20Tab.JPG?raw=true" alt="Analytics By Months Tab">
</p>
<p align="center"><b>Figure:</b> Analytics By Months Tab</p>

## Project Live Demo
Watch the live demo in my LinkedIn post [here](https://www.linkedin.com/posts/muhammad-bilal-ayub_codebasics-python-fastapi-activity-7365910552977534977-63fv?utm_source=share&utm_medium=member_desktop&rcm=ACoAAD04APEBYqCqgcz4clwXp_8hn_MtgwCPeLA).

This project showcases building a full-stack data app with Streamlit + FastAPI + MySQL.
It’s a solid foundation for expense tracking systems and can be extended with more advanced features.

## Let's Connect

I’m excited about building practical data-driven applications like this Expense Tracking System in Python.  
If you’d like to discuss the project, share feedback, or explore collaboration opportunities, feel free to reach out:

- **Email**: bilalayub.connect@gmail.com  
- **LinkedIn**: [https://www.linkedin.com/in/muhammad-bilal-ayub/](https://www.linkedin.com/in/muhammad-bilal-ayub/)

