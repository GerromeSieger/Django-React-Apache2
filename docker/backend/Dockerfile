FROM python:3.9-alpine

WORKDIR /app

ADD ./backend/requirements.txt /app/backend

RUN pip3 install django
RUN pip3 install djangorestframework
RUN pip3 install gunicorn
RUN pip3 install django-cors-headers
RUN pip3 install psycopg2-binary
RUN pip3 freeze > requirements.txt
RUN pip3 install --no-cache-dir -r requirements.txt

COPY ./docker /app/docker

COPY ./backend /app



