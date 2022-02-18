#install  Django
install django-rest-framework
install pillow


**I have also added  field in  profile model 
 of user using API,


In this tutorial we will add field in our model
  name,gender,date_of_birth,phone,profile_image,email
    

# Django Project Setup


pip install -r requirements.txt


1. django-admin startproject restapi .
python manage.py startapp newrest
2. python manage.py migrate
3. python manage.py createsuperuser
4. python manage.py runserver
5. In project settings.py file import os
	


Include app in project *settings.py*


...
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'newrest',
    'rest-framework'
]

To implement that view we need

*urls.py*project urls

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('newrest.urls'),
]

then craete file urls.py in newrest
from . import views
urlpatterns = [
    path('list_data/', views.list_data),
    path('emp_detail/<int:id>', views.employee_details.as_view()),
]

* craete file serializers.py 
Creating a Serializer class
The first thing we need to get started on our Web API is to provide a way of serializing and deserializing the snippet instances into representations such as json. 
We can do this by declaring serializers that work very similar to Django's forms.
Create a file in the snippets directory named serializers.py and add the following.

*in view.py file

in view.py we can post data and also give method 'PUT','GET', 'DELETE'








