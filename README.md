# Pranshu Market - A Flask-Based E-Commerce Platform

Pranshu Market is a simple e-commerce application built using Python's Flask framework. It features user authentication, item management, and a basic transaction system, allowing users to register, log in, and buy or sell items.

## Features

- **User Authentication**: Secure login and registration with hashed passwords.
- **Item Management**: Add, view, purchase, and sell items in the marketplace.
- **Flash Notifications**: Real-time feedback on user actions such as login status and transaction outcomes.
- **Bootstrap Integration**: Responsive and user-friendly design with Bootstrap.
- **Role Management**: Restricted access to marketplace pages for logged-in users only.

## Installation

### Prerequisites
- Python 3.8 or later
- Flask 2.x
- SQLite (pre-configured as the database backend)

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/pranshu-market.git
   cd pranshu-market
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Initialize the database:
   ```bash
   flask shell
   >>> from market import db
   >>> db.create_all()
   >>> exit()
   ```

5. Run the application:
   ```bash
   flask run
   ```

6. Open the application in your browser at [http://127.0.0.1:5000](http://127.0.0.1:5000).

## Project Structure

```plaintext
FLASK/
├── __pycache__/           # Compiled Python files
├── instance/
│   ├── market.db          # SQLite database file
├── market/
│   ├── __pycache__/       # Compiled Python files
│   ├── templates/         # HTML templates for the UI
│   │   ├── includes/      # Modular components for templates
│   │   │   ├── items_modals.html
│   │   │   ├── owned_items_modals.html
│   │   ├── base.html      # Base layout template
│   │   ├── home.html      # Home page template
│   │   ├── login.html     # Login page template
│   │   ├── market.html    # Marketplace page template
│   │   ├── register.html  # Registration page template
│   ├── __init__.py        # App initialization and configuration
│   ├── forms.py           # WTForms for user input validation
│   ├── models.py          # Database models for users and items
│   ├── routes.py          # Application routes
├── venv/                  # Virtual environment
├── run.py                 # Entry point for the application
```

## Usage

1. **Register**: Create an account by filling out the registration form.
2. **Log In**: Log in with your username and password.
3. **Explore**: Browse items available in the marketplace.
4. **Buy/Sell**: Use your virtual budget to purchase items or sell owned items.

## Technologies Used

- **Backend**: Flask (Python)
- **Frontend**: Bootstrap, HTML, CSS
- **Database**: SQLite
- **Authentication**: Flask-Login, Flask-Bcrypt

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request.

## Acknowledgments

- [Flask Documentation](https://flask.palletsprojects.com/)
- [WTForms Documentation](https://wtforms.readthedocs.io/)
- [Bootstrap Documentation](https://getbootstrap.com/)

---

