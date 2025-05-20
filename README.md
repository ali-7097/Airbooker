# Airline Reservation System

A comprehensive web application for airline ticket booking and flight management built with Flask.

## Features

- **User Authentication**: Secure registration and login system with role-based access control
- **Flight Search**: Advanced search functionality for finding flights by destination, date, and more
- **Booking Management**: Complete reservation system with seat selection and e-tickets
- **User Profiles**: Personal dashboard for managing bookings and user information
- **Admin Dashboard**: Administrative tools for managing flights, aircraft, and customer bookings
- **Discount System**: Support for promotional offers and frequent flyer benefits
- **PDF Ticket Generation**: Generate downloadable tickets for confirmed bookings

## Technology Stack

- **Backend**: Flask (Python web framework)
- **Database**: MySQL with SQLAlchemy ORM
- **Authentication**: Flask-Login
- **Forms**: Flask-WTF
- **Migration**: Flask-Migrate
- **Frontend**: HTML, CSS, JavaScript
- **PDF Generation**: WeasyPrint

## Installation

### Prerequisites

- Python 3.8+ 
- MySQL

### Setup

1. Clone the repository
```bash
https://github.com/ali-7097/Airbooker.git
cd airline_reservation_system
```

2. Create and activate a virtual environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install -r airline_reservation_system/requirements.txt
```

4. Configure environment variables
Create a `.env` file in the airline_reservation_system directory with:
```
SECRET_KEY=your_secret_key
DATABASE_URL=mysql+mysqlconnector://username:password@localhost/airline_reservation
MAIL_USERNAME=your_email@gmail.com
MAIL_PASSWORD=your_app_password
```

5. Initialize the database
```bash
cd airline_reservation_system
python reset_db.py
python seed_data.py
```

## Running the Application

```bash
python run.py
```

The application will be available at http://127.0.0.1:5000/

## Demo Accounts

After running the seed_data.py script, the following accounts are available:

- **Regular User**:
  - Email: test@example.com
  - Password: password123

- **Admin User**:
  - Email: admin@airbooker.com
  - Password: admin123

## Project Structure

```
airline_reservation_system/
├── app/
│   ├── models/        # Database models
│   ├── routes/        # Route handlers
│   ├── forms/         # Form definitions
│   ├── templates/     # HTML templates
│   ├── static/        # Static assets
│   └── utils/         # Utility functions
├── migrations/        # Database migrations
├── config.py          # Application configuration
├── run.py             # Application entry point
├── seed_data.py       # Demo data generation
└── requirements.txt   # Dependencies
```
