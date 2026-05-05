# BudgetNest

**BudgetNest** is a Django-based web application designed to help families track and manage their household expenses. Users can register, add family members, record expenses, and generate insightful monthly and yearly spending reports.

---

## Features

- **User Authentication**: Secure signup, login, and logout system
- **Family Member Management**: Add, view, update, and delete family members with their income details
- **Expense Tracking**: Record expenses linked to specific family members with purpose, amount, and date
- **Expense Reports**:
  - View all expenses with total calculation
  - Monthly expense report with filtering
  - Yearly expense report with filtering
  - Combined total expense view (monthly + yearly)
- **User Data Isolation**: Each user can only access their own family members and expenses
- **Responsive UI**: Clean, user-friendly interface with custom CSS styling

---

## Tech Stack

- **Backend**: Django 6.0.3
- **Database**: MySQL
- **Frontend**: HTML, CSS, Bootstrap
- **Language**: Python 3

---

## Prerequisites

Before running this project, ensure you have the following installed:

- [Python 3.10+](https://www.python.org/downloads/)
- [MySQL](https://dev.mysql.com/downloads/installer/)
- pip (Python package manager)

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone <your-github-repo-url>
cd BudgetNestupdated
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> **Note**: `mysqlclient` requires MySQL C connectors. If you face installation issues on Windows, download the appropriate wheel from [https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysqlclient](https://www.lfd.uci.edu/~gohlke/pythonlibs/#mysqlclient) and install it manually:
> ```bash
> pip install <downloaded-wheel-file>.whl
> ```

### 4. Configure Environment Variables

Create a `.env` file in the project root (`BudgetNestupdated/`) and add the following:

```env
SECRET_KEY=django-insecure-_wdgyl8gjx3$=u$oe-*6(ft0^zk&$^)@a44%*x(#_hu+wz(7ob
DB_NAME=budgetnest
DB_USER=root
DB_PASSWORD=6304
DB_HOST=localhost
DB_PORT=3306
DEBUG=True
ALLOWED_HOSTS=127.0.0.1,localhost
```

> **Important**: Generate a new strong `SECRET_KEY` for production. You can generate one using:
> ```bash
> python -c "import secrets; print('SECRET_KEY=' + secrets.token_urlsafe(50))"
> ```

### 5. Create the MySQL Database

Open MySQL and run:
```sql
CREATE DATABASE budgetnest;
```

### 6. Apply Migrations

```bash
python manage.py migrate
```

### 7. Create a Superuser (Optional)

```bash
python manage.py createsuperuser
```

### 8. Run the Development Server

```bash
python manage.py runserver
```

Visit [http://127.0.0.1:8000](http://127.0.0.1:8000) in your browser.

---

## Project Structure

```
BudgetNestupdated/
├── BudgetNest/          # Project configuration
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── accounts/            # Authentication app
│   ├── views.py
│   ├── urls.py
│   └── templates/
├── family/              # Family & expense management app
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
├── static/              # CSS and images
│   └── css/
├── templates/           # Global HTML templates
├── manage.py
└── requirements.txt
```

---

## Important Security Notes

> **Before deploying to production:**
> - Generate a new strong `SECRET_KEY` in your `.env` file
> - Set `DEBUG=False` in your `.env` file
> - Update `ALLOWED_HOSTS` in your `.env` file with your production domain
> - Use strong database credentials and never commit the `.env` file (it is already ignored in `.gitignore`)

---

## Future Enhancements

- [ ] Charts & graphs for expense visualization
- [ ] Income vs expense analytics
- [ ] PDF/Excel export for reports
- [ ] Docker support for easy deployment

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Author

Developed for personal family budget management.
