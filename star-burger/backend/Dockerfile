FROM python:3.12-slim as static
WORKDIR /usr/app/backend

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1


COPY . .
RUN mkdir -p /usr/app/staticfiles/assets
RUN mkdir -p /usr/app/staticfiles/bundles
    
RUN pip install --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt
RUN python3 manage.py collectstatic --noinput
RUN pip install --no-cache-dir gunicorn


FROM static  as gunicorn
WORKDIR /usr/app/backend
RUN pip install gunicorn
EXPOSE 8080
