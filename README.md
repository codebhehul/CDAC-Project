# CDAC-Project
# Restaurant Ordering System

This is a simple restaurant ordering system built with Flask and MySQL. The application allows users to register, login, view restaurant menus, place orders, and see a thank you message after ordering.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Database Setup](#database-setup)
- [Running the Application](#running-the-application)
- [Routing Flow](#routing-flow)
- [Libraries Used](#libraries-used)

## Prerequisites
- Python 3.7 or higher
- MySQL

## Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/restaurant-ordering-system.git
    cd restaurant-ordering-system
    ```

2. **Create a virtual environment:**
    ```bash
    python -m venv venv
    ```

3. **Activate the virtual environment:**

    - On Windows:
        ```bash
        venv\Scripts\activate
        ```

    - On macOS and Linux:
        ```bash
        source venv/bin/activate
        ```

4. **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

## Database Setup
Refer the MyDB.sql


## Running the Application

1. **Set the environment variable for Flask:**
    ```bash
    export FLASK_APP=app.py
    ```

2. **Run the Flask application:**
    ```bash
    flask run
    ```

    By default, the application will be accessible at `http://127.0.0.1:5000`.

## Routing Flow

- `/` -> Redirects to `/login`
- `/register` -> User registration page
- `/login` -> User login page
- `/admin` -> Admin login page
- `/dashboard` -> User dashboard displaying restaurants (requires login)
- `/adminPage` -> Admin page displaying restaurants (requires admin login)
- `/restaurant_menu/<int:restaurant_id>` -> Display menu items of the selected restaurant (requires login)
- `/checkout` -> Checkout page to place an order (requires login)
- `/thankyou` -> Thank you page after placing an order (requires login)
- `/logout` -> Logs out the user and clears the session

## Libraries Used

- Flask
- Flask-Session
- MySQL Connector
- Werkzeug (for password hashing)
- Bootstrap (for frontend styling)

## Additional Notes

- Make sure to replace `'your_secret_key'` in `app.py` with a secure, random value.
- Update the MySQL connection details in `app.py` to match your database configuration.
- The `selected_items` in the checkout process are stored in the session storage of the browser.

Feel free to fork and customize this project according to your needs. Contributions are welcome!
