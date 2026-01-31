# Flask Login Authentication System

A secure and modern login authentication system built with Flask, featuring user registration, secure login, password hashing, and session management. Includes a responsive UI with a beautiful gradient design.

## 🚀 Features

- ✅ User Registration with email validation
- ✅ Secure Login/Logout functionality
- ✅ Password hashing using Werkzeug
- ✅ Session management with Flask-Login
- ✅ MySQL database integration
- ✅ Responsive and modern UI design
- ✅ Flash messages for user feedback
- ✅ Protected routes (login required)

## 🛠️ Technology Stack

- **Backend:** Python Flask
- **Database:** MySQL
- **Frontend:** HTML5, CSS3, Font Awesome Icons
- **Security:** Werkzeug (password hashing), Flask-Login (sessions)
- **Environment:** python-dotenv

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Python 3.7 or higher
- MySQL Server
- pip (Python package manager)

## 🔧 Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/HarshaDesai2005/flask-login-authentication.git
cd flask-login-authentication
```

### 2. Install Python Dependencies

```bash
pip install -r requirements.txt
```

### 3. Set Up MySQL Database

1. Start your MySQL server
2. Create a new database:
   ```sql
   CREATE DATABASE login_auth;
   ```
   > **Note:** The application will automatically create the `users` table on first run.

### 4. Configure Environment Variables

1. Create a `.env` file in the project root directory
2. Add the following configuration:

```env
SECRET_KEY=your-secret-key-here
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=your-mysql-password
MYSQL_DB=login_auth
```

**Important:** 
- Replace `your-secret-key-here` with a secure random string (you can generate one using: `python -c "import secrets; print(secrets.token_hex(32))"`)
- Replace `your-mysql-password` with your actual MySQL root password
- The `.env` file is already in `.gitignore` to protect your credentials

### 5. Run the Application

```bash
python app.py
```

The application will:
- Automatically create the `users` table if it doesn't exist
- Start the Flask development server
- Be accessible at `http://localhost:5000`

## 📁 Project Structure

```
flask-login-authentication/
│
├── app.py                 # Main Flask application
├── config.py              # Configuration settings
├── requirements.txt       # Python dependencies
├── .env                   # Environment variables (not in repo)
├── .gitignore            # Git ignore rules
│
├── static/
│   └── style.css         # CSS styling
│
└── templates/
    ├── home.html         # Welcome page (protected)
    ├── login.html        # Login page
    └── register.html     # Registration page
```

## 🎯 Usage

1. **Register a New Account:**
   - Navigate to `http://localhost:5000`
   - Click "Register" or go to `/register`
   - Fill in your name, email, and password
   - Confirm your password
   - Submit the form

2. **Login:**
   - Go to `/login`
   - Enter your email and password
   - You'll be redirected to the home page upon successful login

3. **Logout:**
   - Click the "Logout" button in the navigation bar
   - You'll be redirected back to the login page

## 🔒 Security Features

- Passwords are hashed using Werkzeug's secure password hashing
- Session management prevents unauthorized access
- Environment variables keep sensitive data secure
- SQL injection protection through parameterized queries

## 📝 Notes

- The application runs in debug mode by default (suitable for development)
- For production, set `debug=False` in `app.py`
- Make sure your MySQL server is running before starting the application
- The `.env` file should never be committed to version control

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/HarshaDesai2005/flask-login-authentication/issues).

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

## 👤 Author

**Harsha Desai**

- GitHub: [@HarshaDesai2005](https://github.com/HarshaDesai2005)

---

⭐ If you found this project helpful, please consider giving it a star!
