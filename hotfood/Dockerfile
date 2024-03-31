FROM python:3.9 as build
COPY . /code
WORKDIR /code/Hot-Food
RUN pip3 install pipenv && pip3 install ta-lib && pipenv install -r requirements.txt && pipenv shell && apt-get update && apt-get install -y rabbitmq-server && service rabbitmq-server start
WORKDIR /code/Hot-Food/src/
CMD python manage.py makemigrations
CMD python manage.py migrate
CMD python manage.py runserver 
