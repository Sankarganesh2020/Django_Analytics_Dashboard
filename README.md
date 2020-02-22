# Django_Analytics_Dashboard

### Bootstrap a Django project with this command

    django-admin startproject analytics_project

### go to folder analytics_project

    cd analytics_project

### Start the server with a console command

    python manage.py runserver

### Create a new app in your project. Let’s name it dashboard

    python manage.py startapp dashboard

### Register the app in the project(append the app's name to the INSTALLED_APPS list).

### how can we translate our model class into a database table?

#### This is where the concept of migration comes in handy. Migration is simply a file that describes which changes must be applied to the database. Every time we need to create a database based on the model described by Python classes, we use migration.

    python manage.py makemigrations dashboard

### Here we specified that the app should tell Django to apply migrations for the dashboard app's models.

### After creating a migration file, apply migrations described in it and create a database:

    python manage.py migrate dashboard

### Let's create instances of our Order class. For this, we'll use the Django shell - it's similar to the Python shell but allows accessing the database and creating new entries. So, start the Django shell

    python manage.py shell