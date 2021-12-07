# Django_HelloApp_Response-Object

Here are steps as follows:

STEP 1: First, I have create project (ProjectHello) using the command (py -m django startproject ProjectHello). This 
        will creat a project folder.

STEP 2: Now, using the cmd need to go under folder ProjectHello. 

STEP 3: You need to create an app using the command (py manage.py startapp HelloApp). This will create an app folder.

STEP 4: Need to write the code for following Under folder HelloApp:

(a) Urls.py

from django.urls import path
from . import views

urlpatterns = [
    path('', views.show),
]

(b) views.py

from django.http import JsonResponse 

-- Create your views here.
def show(request):
    return JsonResponse({"Message": "Hello World!"})

STEP 5: Need to write the code for following under folder projecthello

(a) urls.py

from django.contrib import admin
from django.urls import path, include

urlpatterns = [
    path('admin/', admin.site.urls),
    path('', include('HelloApp.urls')),
]


STEP 6: Run the code using the following code (py manage.py runserver)
