# Django-docker
Django API with docker

## to create a project inside of container
docker-compose run  --rm app sh -c "django-admin startproject app ."
## to create an app inside of container
docker-compose run  --rm app sh -c "python manage.py startapp core"

## Create migrations inside of container
docker-compose run  --rm app sh -c "python manage.py makemigrations"

## Run migrations inside of container
docker-compose run  --rm app sh -c "python manage.py wait_for_db && python manage.py migrate"

## to create superuse inside of container
docker-compose run  --rm app sh -c "python manage.py createsuperuser"

## to run tests inside of container and lint
docker-compose run  --rm app sh -c "python manage.py test && flake8"