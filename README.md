# University Management System

![Django](https://img.shields.io/badge/Django-092E20?logo=django\&logoColor=white)
![Stripe](https://img.shields.io/badge/Stripe-008CDD?logo=stripe\&logoColor=white)
![Twilio](https://img.shields.io/badge/Twilio-F22F46?logo=twilio\&logoColor=white)

A comprehensive Django-based university management system with secure payment processing, SMS notifications, and email integration.

---

## ✨ Key Features

* **User Management**

  * Role-based authentication (Admin, Faculty, Students)
  * Password reset functionality
  * Profile management

* **Academic Features**

  * Course registration system
  * Grade tracking
  * Attendance management

* **Payment System**

  * Secure fee payments via Stripe
  * Payment history tracking
  * Receipt generation

* **Communication**

  * Email notifications (Gmail integration)
  * SMS alerts (Twilio integration)
  * Announcement system

* **Admin Dashboard**

  * Comprehensive data management
  * Analytics and reporting
  * System configuration

---

## 🚀 Getting Started

### Prerequisites

* Python 3.8+
* PostgreSQL (recommended for production)
* Stripe, Twilio, and Gmail accounts

### Installation

1. **Clone the repository**

```bash
git clone https://github.com/vk0595429/university-django.git
cd university-django
```

2. **Set up virtual environment**

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/MacOS
source venv/bin/activate
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Configure environment variables**
   Create `.env` file in `myproject/` directory:

```env
SECRET_KEY=your_django_secret_key
DEBUG=True
DATABASE_URL=postgres://user:password@localhost/dbname

# Email Configuration
EMAIL_HOST_USER=your_email@gmail.com
GMAIL_APP_PASSWORD=your_app_password

# Twilio Configuration
TWILIO_ACCOUNT_SID=your_account_sid
TWILIO_AUTH_TOKEN=your_auth_token
TWILIO_PHONE_NUMBER=+1234567890

# Stripe Configuration
STRIPE_API_KEY=your_stripe_key
STRIPE_WEBHOOK_SECRET=your_webhook_secret
```

5. **Run migrations**

```bash
python manage.py migrate
```

6. **Create superuser**

```bash
python manage.py createsuperuser
```

7. **Run development server**

```bash
python manage.py runserver
```

Access the application at [http://localhost:8000](http://localhost:8000).

---

## 🛠 Project Structure

```
university-django/
├── myproject/               # Main project configuration
├── accounts/                # User authentication app
├── courses/                 # Course management app
├── payments/                # Payment processing app
├── notifications/           # Communication app
├── static/                  # Static files
├── templates/               # HTML templates
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

---

## 🔧 Deployment

### Production Recommendations

* Web Server: Nginx
* Application Server: Gunicorn or uWSGI
* Database: PostgreSQL
* Environment: Linux server (Ubuntu recommended)

### Deployment Steps

1. Set `DEBUG=False` in `.env`
2. Configure allowed hosts in `settings.py`:

```python
ALLOWED_HOSTS = ['yourdomain.com', 'www.yourdomain.com']
```

3. Collect static files:

```bash
python manage.py collectstatic
```

4. Set up production database (PostgreSQL recommended)
5. Configure HTTPS with SSL certificate

---

## 📚 Documentation

* API Documentation (Coming Soon)
* Admin Guide
* User Manual

---

## 📧 Contact

**Vishal Kumar Chaurasia**

* Email: [vk0595429@gmail.com](mailto:vk0595429@gmail.com)
* GitHub: [@vk0595429](https://github.com/vk0595429)
* LinkedIn: [Vishal Kumar Chaurasia](https://www.linkedin.com/in/vishalkumarchaurasia)
