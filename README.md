# Django-docker
Django API with docker

## to create a project inside of container
docker-compose run  --rm app sh -c "django-admin startproject app ."
## to create an app inside of container
docker-compose run  --rm app sh -c "python manage.py startapp core"

## to run tests inside of container
docker-compose run  --rm app sh -c "python manage.py test && flake8"