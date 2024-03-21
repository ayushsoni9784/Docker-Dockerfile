FROM ubuntu as build
RUN apt-get update && apt-get install -y python3 && apt install python3-pip
COPY . /code
RUN pip install pipenv && pipenv install -r requirements.txt && pipenv shell && sudo apt-get install rabbitmq-server && service rabbitmq-server start

CMD 
