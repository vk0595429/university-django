# University Django Project

A Django web application project for educational purposes. This project is cleaned from all sensitive data and ready for development or deployment.

---

## Features

* User authentication and authorization
* Custom apps and models
* Responsive frontend with Django templates
* Integration with Gmail, Twilio, and Stripe APIs
* Secure handling of sensitive keys via `.env`
* Ready for development and deployment
* Logging and error tracking
* Admin panel for managing users and data

---

## Setup

1. **Clone the repository**

```bash
git clone https://github.com/vk0595429/university-django.git
cd university-django
```

2. **Create a virtual environment (recommended)**

```bash
python -m venv venv
venv\Scripts\activate   # Windows
source venv/bin/activate  # Linux / macOS
```

3. **Install dependencies**

```bash
pip install -r requirements.txt
```

4. **Create your `.env` file**

Create a `.env` file in the `myproject/` directory and add your secret keys:

```env
GMAIL_APP_PASSWORD=your_gmail_app_password
TWILIO_ACCOUNT_SID=your_twilio_sid
TWILIO_AUTH_TOKEN=your_twilio_auth_token
STRIPE_API_KEY=your_stripe_key
```

> **Important:** `.env` is ignored by Git and should never be committed.

5. **Apply migrations**

```bash
python manage.py migrate
```

6. **Run the development server**

```bash
python manage.py runserver
```

Access the app at [http://127.0.0.1:8000](http://127.0.0.1:8000).

---

## Deployment

* Use environment variables for secrets (do not commit `.env`).
* Recommended: Gunicorn + Nginx for production.
* Collect static files before deployment:

```bash
python manage.py collectstatic
```

* Set DEBUG=False in `.env` for production.
* Configure allowed hosts in `settings.py`.
* Enable HTTPS and SSL certificates.

---

## Security

* `.env` removed from all Git history.
* GitHub push protection will prevent accidental secret commits.
* Always regenerate keys if they were exposed.
* Regularly update dependencies to patch vulnerabilities.
* Validate user inputs and sanitize data.

---

## Contribution

1. Fork the repo.
2. Create a branch for your feature/fix.
3. Make changes and commit safely.
4. Push and open a pull request.
5. Ensure all tests pass before submitting a pull request.

---

## Additional Information

* Uses Django 5.2 or higher.
* Includes sample data for testing.
* Supports SQLite for development and PostgreSQL for production.
* Built with modular apps for easy scalability.
* Includes basic unit tests.
* Logging is configured for development and production.
