BLOG Project

This chapter will cover the following topics:
• Installing Python
• Creating a Python virtual environment
• Installing Django
• Creating and configuring a Django project
• Building a Django application
• Designing data models
• Creating and applying model migrations
• Creating an administration site for your models
• Working with QuerySets and model managers
• Building views, templates, and URLs
• Understanding the Django request/response cycle 

Command Line Shots:

1. python -m venv blog_env
2. source blog_env/bin/activate
3. pip install Django~=4.1.0
4. django-admin startproject blog
5. django-admin startapp blog_app
6. python manage.py runserver 127.0.0.1:8001 --settings=blog.settings
7. Ctrl+c
8. python manage.py makemigrations
9. python manage.py migrate
9. python manage.py runserver
10. python manage.py createsuperuser
11. python manage.py shell
  - from django.contrib.auth.models import User
  - from blog_app.models import Post
  - user = User.objects.get(username='admin')
  - post = Post(title='Another post',
                 slug='another-post',
                 body='Post body.',
                 author=user)
  - post.save()
  - post.title = 'New title'
  - post.save()





Trade Offs:

1. In the INSTALLED_APPS in the settings file I tried to add up 'blog.apps.Blog_AppConfig' but it doesn't accept underlines then 'blog.apps.BlogAppConfig' worked smoothly.