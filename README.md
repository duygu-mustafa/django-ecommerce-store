# Jewellery Shop — Django E‑commerce (SoftUni Course Project)


A small, instructional e‑commerce web application implemented with Django. Built as part of the SoftUni "Python Web Frameworks" course (September 2020), this project demonstrates a simple online jewellery shop with product browsing, cart and checkout flows, user accounts, and basic administration.

## Features

- Browse and filter products
- View product details
- Add / update / remove items from a shopping cart
- User registration, login and profile management
- Manage shipping addresses and mark defaults
- Favorite products (user favorites)
- Place orders (checkout for authenticated users)
- Admin interface for managing products and orders

## Technology Stack

- Python 3.x
- Django 3.1
- PostgreSQL (development settings included)
- HTML/CSS templates (Django templates)

## Repository Layout

- `shop/` — product models, views and templates
- `accounts/` — user registration, profile and addresses
- `cart/` — cart logic and cart views
- `order/` — order creation and checkout
- `templates/` — project templates and partials
- `static/` — CSS and images
- `web_frameworks/` — Django project settings and URL routing

See the project files for full details.

## Setup / Local Development

1. Clone the repository:

	git clone <repo-url>
	cd softuni-web-project

2. Create and activate a virtual environment:

	python3 -m venv .venv
	source .venv/bin/activate

3. Install dependencies:

	pip install -r requirements.txt

4. Configure environment-specific settings:

- The repository contains a development `web_frameworks/settings.py` configured for PostgreSQL. Do not commit secrets. Recommended options:
  - Set environment variables for `SECRET_KEY`, database credentials, and `DEBUG` and modify `web_frameworks/settings.py` to read them, or
  - Edit `web_frameworks/settings.py` locally for quick testing (not for production).

5. Create the database and run migrations:

	# ensure PostgreSQL is running and a database exists matching your settings
	python manage.py migrate

6. (Optional) Create a superuser for the admin site:

	python manage.py createsuperuser

7. Run the development server:

	python manage.py runserver

8. Open your browser at `http://127.0.0.1:8000/`.

## Running Tests

Run the Django test suite:

	python manage.py test

## Deployment Notes

- Set `DEBUG = False` and configure `ALLOWED_HOSTS`.
- Serve static files with a proper web server (e.g., Nginx) and run `python manage.py collectstatic`.
- Use Gunicorn/Uvicorn behind a reverse proxy for production.
- Store secrets and database credentials in environment variables or a secrets manager.

## Security / Credentials

The included `web_frameworks/settings.py` contains a development configuration (and example DB credentials). Remove or override any hardcoded secrets before publishing or deploying the project.

## Suggested Improvements (for portfolio polish)

- Add a clear sample data fixture or script to populate products for screenshots.
- Replace the hardcoded secret key and DB credentials with environment-driven configuration.
- Add unit / integration tests for core flows (cart, checkout, account management).
- Add screenshots or a short demo GIF to this README.

## License

This project is published under the MIT License.


![Homepage screenshot](docs/screenshot.png)