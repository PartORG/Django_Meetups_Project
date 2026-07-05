# Django_Meetups_Project

A simple example of Django capabilities.

[![Python](https://img.shields.io/badge/python-3.10-blue.svg)](https://www.python.org/downloads/release/python-3100/)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Package Manager](https://img.shields.io/badge/package-manager-pip-yellow.svg)](https://pip.pypa.io/en/stable/installation/)
[![Framework](https://img.shields.io/badge/framework-Django-red.svg)](https://www.djangoproject.com/)

Django_Meetups_Project is a simple example of Django capabilities. It includes models, views, templates, and migrations for managing meetups. The project uses SQLite as the database.

## Table of Contents

- [Features](#features)
- [How It Works](#how-it-works)
- [Technology Stack](#technology-stack)
- [Requirements](#requirements)
- [Installation](#installation)
- [Configuration](#configuration)
- [Quick Start](#quick-start)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Development](#development)
- [Limitations](#limitations)
- [License](#license)

## Features

### Meetup Management
- **Models**: Define the structure of data for meetups, participants, and locations.
- **Views**: Handle user requests and interact with models to perform operations like creating, reading, updating, and deleting meetups.
- **Templates**: Render HTML pages dynamically based on the data retrieved from the database.

## How It Works

Django_Meetups_Project follows a typical Django project structure. The main components are:

1. **Models**: Define the data schema using Django's ORM.
2. **Views**: Handle business logic and interact with models to perform operations.
3. **Templates**: Generate HTML content dynamically based on the data retrieved from the database.

## Technology Stack

| Technology | Purpose |
|------------|---------|
| Python     | The programming language used for development. |
| Django     | A high-level Python web framework that encourages rapid development and clean, pragmatic design. |
| SQLite     | A lightweight disk-based database that doesn’t require a separate server process and allows accessing the database using a nonstandard variant of the SQL query language. |

## Requirements

- Python 3.10
- Django 4.0 or later

## Installation

To install Django_Meetups_Project, follow these steps:

```bash
git clone https://github.com/PartORG/Django_Meetups_Project.git
cd Django_Meetups_Project
pip install -r requirements.txt
```

## Configuration

The project uses environment variables for configuration. You can set the following variables in your `.env` file:

- `SECRET_KEY`: A secret key used to sign data.
- `DEBUG`: Set to `True` during development and `False` in production.

## Quick Start

To run the project, execute the following command:

```bash
python manage.py runserver
```

This will start a development server on `http://127.0.0.1:8000/`.

## Usage

### Creating a Meetup

To create a new meetup, navigate to `/admin` and log in with the provided credentials.

### Viewing Meetups

You can view all meetups by visiting the home page (`/`).

### Registering for a Meetup

Participants can register for a meetup by visiting the meetup details page and clicking on the "Register" button.

## Project Structure

```
Django_Meetups_Project/
├── manage.py
├── django_course_site/
│   ├── __init__.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── meetups/
│   ├── __init__.py
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── migrations/
│   │   ├── 0001_initial.py
│   │   ├── 0002_meetup_image.py
│   │   ├── 0003_location.py
│   │   ├── 0004_meetup_location.py
│   │   ├── 0005_participant_meetup_participants.py
│   │   ├── 0006_meetup_date_meetup_organizer_email.py
│   │   └── __init__.py
│   ├── models.py
│   ├── static/
│   │   └── meetups/
│   │       ├── styles/
│   │       │   ├── all-meetups.css
│   │       │   ├── base.css
│   │       │   ├── meetup-detail.css
│   │       │   └── registration-confirmation.css
│   │       └── uploads/
│   │           ├── images/
│   │               ├── mountain.jpg
│   │               ├── planet.jpeg
│   │               ├── planet_0mvUQi9.jpeg
│   │               ├── planet_3Acjl2H.jpeg
│   │               └── planet_aZXtUz8.jpeg
│   ├── templates/
│   │   └── meetups/
│   │       ├── base/
│   │       │   └── base.html
│   │       ├── includes/
│   │       │   └── meetup-item.html
│   │       ├── index.html
│   │       ├── meetup-details.html
│   │       └── registration-success.html
│   ├── tests.py
│   ├── urls.py
│   └── views.py
└── uploads/
    └── images/
        ├── mountain.jpg
        ├── planet.jpeg
        ├── planet_0mvUQi9.jpeg
        ├── planet_3Acjl2H.jpeg
        └── planet_aZXtUz8.jpeg
```

## Development

The project follows a standard Django development workflow. You can run migrations, create superusers, and perform other tasks using the `manage.py` script.

```bash
python manage.py migrate
python manage.py createsuperuser
```

## Limitations

- The project is a simple example and does not include advanced features like authentication, authorization, or complex forms.
- It uses SQLite for simplicity, but production environments should use more robust databases like PostgreSQL or MySQL.

## License

Django_Meetups_Project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.