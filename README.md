# Booking Appointment API

A RESTful API built with Django and Django REST Framework for managing appointment bookings.

## Features

- User authentication and authorization
- Create, read, update, and delete appointments
- Manage availability schedules
- Search and filter appointments

## Requirements

- Python 3.8+
- Django 4.0
- Django REST Framework 3.14.0

## Installation

1. Clone the repository:
   ```
   git clone <repository-url>
   cd booking-appointment-api
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```

4. Apply migrations:
   ```
   python manage.py migrate
   ```

5. Create a superuser (admin):
   ```
   python manage.py createsuperuser
   ```

6. Run the development server:
   ```
   python manage.py runserver
   ```

## API Endpoints

### Authentication
- `POST /api/token/` - Obtain JWT token
- `POST /api/token/refresh/` - Refresh JWT token

### Users
- `GET /api/users/` - List users
- `POST /api/users/` - Create user
- `GET /api/users/{id}/` - Get user details
- `PUT /api/users/{id}/` - Update user
- `DELETE /api/users/{id}/` - Delete user

### Appointments
- `GET /api/appointments/` - List appointments
- `POST /api/appointments/` - Create appointment
- `GET /api/appointments/{id}/` - Get appointment details
- `PUT /api/appointments/{id}/` - Update appointment
- `DELETE /api/appointments/{id}/` - Delete appointment

## Configuration

You can configure the application by creating a `.env` file in the project root with the following variables:

```
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///db.sqlite3
```

## Testing

Run tests with:

```
python manage.py test
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
