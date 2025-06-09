
# 📘 Learning Log

A web application to help users keep track of the topics they’re learning about. Users can create accounts, make topics, and add journal-style entries for each topic.

🔗 **Live App**: https://learning-logs-r8se.onrender.com/

---

## 🚀 Features

- User registration and login system  
- Add and view learning topics  
- Add, view, and edit topic entries  
- Bootstrap-based responsive UI  
- Admin panel for superusers  
- SQLite-based local development  

---

## 🛠️ Tech Stack

- **Backend**: Django 5.2.2  
- **Frontend**: HTML, CSS, Bootstrap 4  
- **Database**: SQLite (dev), PostgreSQL (prod-ready via `dj-database-url`)  
- **Deployment**: Render.com  
- **Others**: Gunicorn, Whitenoise for static files  

---

## 📁 Project Structure

```
learning_log/
│
├── learning_logs/     # Core app handling topics and entries
├── users/             # User authentication and profile handling
├── templates/         # HTML templates
├── db.sqlite3         # Local DB
├── manage.py          # Django project manager
├── build.sh           # Deployment build script
├── requirements.txt   # Python dependencies
└── ll_env/            # Virtual environment (not required in repo)
```

---

## 🧪 Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/learning_log.git
   cd learning_log
   ```

2. **Create Virtual Environment & Install Requirements**
   ```bash
   python -m venv venv
   source venv/bin/activate  # or venv\Scripts\activate on Windows
   pip install -r requirements.txt
   ```

3. **Apply Migrations**
   ```bash
   python manage.py migrate
   ```

4. **Create Superuser (Optional)**
   ```bash
   python manage.py createsuperuser
   ```

5. **Run Locally**
   ```bash
   python manage.py runserver
   ```

---

## 📦 Deployment (Render)

Deployment is configured for Render. The `build.sh` file handles:

- Installing dependencies  
- Collecting static files  
- Running database migrations  

Set the following environment variables on Render:

- `SECRET_KEY`  
- `DEBUG = False`  
- `DATABASE_URL` (for PostgreSQL)  
- `ALLOWED_HOSTS` (your domain or `*` for testing)

---

## 📚 Requirements

<details>
<summary>Click to expand</summary>

```
asgiref==3.8.1  
beautifulsoup4==4.13.4  
click==8.2.1  
colorama==0.4.6  
dj-database-url==3.0.0  
Django==5.2.2  
django-bootstrap4==25.1  
django-heroku==0.3.1  
gunicorn==23.0.0  
h11==0.16.0  
packaging==25.0  
psycopg2==2.9.10  
psycopg2-binary==2.9.10  
setuptools==80.9.0  
soupsieve==2.7  
sqlparse==0.5.3  
typing_extensions==4.14.0  
tzdata==2025.2  
uvicorn==0.34.3  
wheel==0.45.1  
whitenoise==6.9.0  
```

</details>


## Acknowledgements

This website was built as a project inspired by the book Python Crash Course by Eric Matthes, with additional enhancements and styling to offer a smoother and more interactive experience. 

