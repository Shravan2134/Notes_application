# Flask Web Application

This is a simple Flask web application with user authentication and note-taking functionality.  
It uses MySQL as the database backend and SQLAlchemy as the ORM.

## Features

- User registration (sign up)
- User login/logout
- Add and delete personal notes
- Passwords securely hashed
- Flash messages for feedback

## Project Structure

```
Flask_web_application/
│
├── app.py
├── instance/
├── venv/
├── web_server/
│   ├── __init__.py
│   ├── auth.py
│   ├── models.py
│   ├── views.py
│   └── templates/
│       ├── base.html
│       ├── home.html
│       ├── login.html
│       └── sign_up.html
```

## Setup Instructions

### 1. Clone the repository

```sh
git clone <repo-url>
cd Flask_web_application
```

### 2. Create and activate a virtual environment

```sh
python3 -m venv venv
source venv/bin/activate
```

### 3. Install dependencies

```sh
pip install flask flask_sqlalchemy flask_login pymysql
```

### 4. Configure the database

Edit `web_server/__init__.py` and set your MySQL credentials:

```python
DB_NAME = "your_db_name"
DB_USER = "your_db_user"
DB_PASSWORD = "your_db_password"
DB_HOST = "localhost"
```

Make sure the database exists and the user has privileges.

### 5. Run the application

```sh
python3 app.py
```

The app will be available at [http://127.0.0.1:5000](http://127.0.0.1:5000).

## Usage

- Visit `/sign-up` to create a new account.
- Log in at `/login`.
- Add and delete notes from the home page.

## Notes

- Passwords are hashed using `pbkdf2:sha256`.
- All templates are in `web_server/templates/`.
- The app uses Flask blueprints for modularity.

## License

MIT License
