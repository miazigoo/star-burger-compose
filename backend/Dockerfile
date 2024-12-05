FROM python:3.10.12

WORKDIR /star-burger

COPY . .

RUN pip3 install --no-cache-dir --upgrade pip
RUN pip3 install --no-cache-dir -r requirements.txt
RUN python3 manage.py collectstatic --noinput
EXPOSE 8080
