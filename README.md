Django Course Management System
Overview
This project is a Django application for managing courses. It includes features for listing, viewing, creating, updating, and deleting courses. The project uses Django 5.0.7 and leverages python-decouple for managing sensitive settings.

Requirements
Python 3.8 or later
Django 5.0.7
python-decouple
Setup
1. Clone the Repository
bash
Копировать код
git clone <repository_url>
cd <repository_directory>
2. Create a Virtual Environment
bash
Копировать код
python -m venv venv
source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
3. Install Dependencies
bash
Копировать код
pip install -r requirements.txt
4. Set Up Environment Variables
Create a .env file in the root directory of your project and add the following environment variables:

makefile
Копировать код
SECRET_KEY=your-secret-key
DEBUG=True
ALLOWED_HOSTS=localhost,127.0.0.1
5. Run Migrations
bash
Копировать код
python manage.py migrate
6. Collect Static Files
bash
Копировать код
python manage.py collectstatic
7. Create a Superuser
bash
Копировать код
python manage.py createsuperuser
8. Run the Development Server
bash
Копировать код
python manage.py runserver
Project Structure
project/ - Main project directory containing settings and WSGI configuration.
courses/ - Django app for managing courses.
models.py - Defines the data models for the app.
views.py - Contains the views for displaying and handling courses.
forms.py - Contains forms for course creation and updates.
urls.py - Defines URL patterns for the app.
templates/ - Contains HTML templates for rendering views.
static/ - Contains static files such as CSS and JavaScript.
media/ - Directory for uploaded media files.
Endpoints
/courses/ - List all courses.
/courses/<slug>/ - View details of a specific course.
/courses/add/ - Add a new course.
/courses/<slug>/edit/ - Edit an existing course.
/courses/<slug>/delete/ - Delete a course.
Messages
The application uses Django's messages framework to display feedback to users:

Success messages: Inform users of successful operations (e.g., course creation or update).
Error messages: Inform users of errors (e.g., validation errors).
License
