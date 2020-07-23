# Django Api

NOTES BELOW ARE UNORGANISED (rough notes from hackathon day) AND MAY BE INCORRECT...NEED TO EDIT

### References
https://www.django-rest-framework.org/tutorial/2-requests-and-responses/


https://towardsdatascience.com/scheduled-web-scraping-with-django-and-heroku-e832e1363c7a

https://codeburst.io/beginners-guide-to-deploying-a-django-postgresql-project-on-google-cloud-s-flexible-app-engine-e3357b601b91

https://realpython.com/beautiful-soup-web-scraper-python/

https://docs.graphene-python.org/projects/django/en/latest/tutorial-plain/

### 
pip freeze 
pip freeze > requirements.txt (will copy to requirements.txt)

## Terminal commands to create project

```bash
cd <project-directory>

# create virtual env called venv, and activate it
python3 -m venv venv
source venv/bin/activate   

# install
pip install django
pip install djangorestframework

# create a project called api
django-admin startproject api .    

# run the server 
python3 manage.py runserver
```

### python shell
python manage.py shell

### file stucture

- file ```urls.py``` has the routes for the app, e.g.
    ```
    from django.contrib import admin
    from django.urls import path

    urlpatterns = [
        path('admin/', admin.site.urls),
    ]
    ```
    The second argument in ```path('admin/', admin.site.urls)``` is what we want to render.



### set up migrations
```
# migrations sets up the database db.sqlite3 i believe
python manage.py makemigrations
python manage.py migrate
```
need to run migrations each time you change the database in models.py

### create a superuser:
```
python manage.py createsuperuser
```

## python class
class Parent():
    number = 5

class Child(Parent):
    pass

kiddo = Child()
kiddo.number

#

class.objects.all()

## django rest framework

### imports
from folder.file import Class 