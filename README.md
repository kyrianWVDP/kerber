# Care Bear Medical Monitoring Application

This is a Flask web application for monitoring patient health data. It allows users to register as patients or doctors, log in, and view or set medical alarms.

## Features

- User Registration and Login
- Dashboard for Doctors and Patients
- Setting Medical Alarms
- Viewing Patient Measurements

## Requirements

- Python 3.10+
- Flask
- Flask-WTF
- Flask-Login
- Flask-SQLAlchemy
- Flask-Migrate
- Pygame
- Email-Validator
- Flask-Mail

## Installation

1. **Clone the repository:**
    ```sh
    git clone https://github.com/yourusername/carebear.git
    cd carebear
    ```

2. **Create and activate a virtual environment:**
    ```sh
    python -m venv .venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    ```

3. **Install the required packages:**
    ```sh
    pip install -r requirements.txt
    ```

4. **Set up environment variables:**
    Create a `.env` file in the root of your project and add the following configurations:
    ```env
    SECRET_KEY=your_secret_key
    SQLALCHEMY_DATABASE_URI=sqlite:///site.db
    MAIL_SERVER=smtp.example.com
    MAIL_PORT=587
    MAIL_USE_TLS=True
    MAIL_USERNAME=your_email@example.com
    MAIL_PASSWORD=your_password
    ```

5. **Initialize the database:**
    If you choose to use Flask-Migrate for migrations:
    ```sh
    flask db init
    flask db migrate -m "Initial migration"
    flask db upgrade
    ```
    Alternatively, you can manually create the database schema as needed.

6. **Run the application:**
    ```sh
    flask run --host=0.0.0.0 --port=5000
    ```

## Usage

### Register

Visit `/register` to create a new user account. Choose whether you are a patient or a doctor.

### Login

Visit `/login` to log in to your account.

### Dashboard

After logging in, you will be redirected to your dashboard. Doctors can view their patients, and patients can view their medical data and set alarms.

### Setting Alarms

Patients can set medication alarms to be reminded daily at a specific time or alert alarms that will notify doctors if health parameters are out of range.

### Viewing Measurements

Doctors can view the historical health data of their patients.

## Troubleshooting

- **Module Not Found Error:** Ensure all required packages are installed and the virtual environment is activated.
- **Database Errors:** Ensure the database has been initialized and migrated correctly.

## Contributing

Feel free to fork the repository and submit pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License.
