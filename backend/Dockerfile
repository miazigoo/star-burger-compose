FROM python:3.9-slim as backend

WORKDIR /star-burger

COPY . .

RUN mkdir -p /star-burger/assets
RUN mkdir -p /star-burger/bundles

RUN pip3 install --no-cache-dir --upgrade pip
RUN pip3 install --no-cache-dir -r requirements.txt
RUN python3 manage.py collectstatic --noinput

