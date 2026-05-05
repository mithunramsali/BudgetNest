# 💰 BudgetNest

**BudgetNest** is a full-stack Django web application that helps families track, manage, and analyze household expenses efficiently.

It allows users to manage family members, record expenses, and generate structured financial reports for better decision-making.

---

## 🚀 Key Features

- 🔐 Authentication System
  - Secure user signup, login, logout
  - User-specific data isolation

- 👨‍👩‍👧 Family Management
  - Add, update, delete family members
  - Track individual income details

- 💸 Expense Tracking
  - Record expenses with:
    - Amount
    - Purpose
    - Date
    - Linked family member

- 📊 Reports & Insights
  - Total expense overview
  - Monthly filtering
  - Yearly filtering
  - Combined reports

- 🎨 Responsive UI
  - Clean and user-friendly interface
  - Built with Bootstrap + custom CSS

---

## 🛠️ Tech Stack

| Layer        | Technology        |
|-------------|------------------|
| Backend      | Django 6.x        |
| Database     | MySQL             |
| Frontend     | HTML, CSS, Bootstrap |
| Language     | Python 3.x        |

---

## ⚙️ Installation & Setup

### 1. Clone the repository
git clone https://github.com/your-username/budgetnest.git
cd budgetnest

### 2. Create virtual environment
python -m venv venv
venv\Scripts\activate

### 3. Install dependencies
pip install -r requirements.txt

### 4. Configure environment variables

Create `.env` file:

SECRET_KEY=your-secret-key
DEBUG=True

DB_NAME=budgetnest
DB_USER=root
DB_PASSWORD=your_password
DB_HOST=localhost
DB_PORT=3306

ALLOWED_HOSTS=127.0.0.1,localhost

### 5. Create database

CREATE DATABASE budgetnest;

### 6. Run migrations
python manage.py migrate

### 7. Create superuser (optional)
python manage.py createsuperuser

### 8. Run server
python manage.py runserver

---

## 📂 Project Structure

budgetnest/
│
├── BudgetNest/
├── accounts/
├── family/
├── static/
├── templates/
├── manage.py
└── requirements.txt

---

## 🔐 Security Notes

- Never commit `.env`
- Set DEBUG=False in production
- Use a strong SECRET_KEY
- Secure DB credentials

---

## 📈 Future Improvements

- Expense charts
- Export reports (PDF/Excel)
- API integration
- Mobile app version

---

## 📄 License

MIT License

---

## 👨‍💻 Author

Developed by Mithun R
