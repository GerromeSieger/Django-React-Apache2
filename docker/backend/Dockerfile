FROM python:3.9-alpine

WORKDIR /app

COPY django-react-postgres/backend/djangoreactproject /app

ADD django-react-postgres/backend/requirements.txt /app/backend

RUN pip3 install django
RUN pip3 install djangorestframework
RUN pip3 install gunicorn
RUN pip3 install django-cors-headers
RUN pip3 install psycopg2-binary
RUN pip3 freeze > requirements.txt
RUN pip3 install --no-cache-dir -r requirements.txt

COPY django-react-postgres/docker /app/docker

COPY django-react-postgres/docker/backend/wsgi-entrypoint.sh /

ENTRYPOINT ["sh", "/wsgi-entrypoint.sh"]


