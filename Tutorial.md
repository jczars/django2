# Instalando Django
https://www.digitalocean.com/community/tutorials/how-to-install-django-and-set-up-a-development-environment-on-ubuntu-16-04

## Step 1 — Install Python and pip
sudo apt-get update && sudo apt-get -y upgrade
sudo apt-get install python3
python3 -V
## Step 2 — Install virtualenv
pip3 install virtualenv
virtualenv --version

## Step 3 — Install Django
virtualenv env3
. env3/bin/activate
pip install django
django-admin --version

## Step 4 — Creating a Django Test Project
### Setting Firewall Rules
sudo ufw allow 8000

### Starting the Project
django-admin startproject testsite
cd testsite
ls

### Start and View your Website
nano ~/django2/testsittestsite/settings.py


# Tutorial 2
https://djangoforbeginners.com/

## Chapter 1: Initial Setup
### Install Git
sudo apt-get install git-all

## Chapter 2: Hello World app
### Initial Setup
mkdir helloworld
cd helloworld

### create projectls
https://djangoforbeginners.com/hello-world/
django-admin.py startproject helloworld_project

## Create an app
./manage.py startapp pages

## register
settings.py
INATALLED_APPS = [ .. pages',]

## Views and URLConfs
from django.http import HttpResponse

def homePageView(request):
    return HttpResponse('Hello, World!')
## Create pages/urls.py 
touch pages/urls.py
from django.urls import path

from . import views

urlpatterns = [
    path('', views.homePageView, name='home')
]
