FROM node:16.16.0 as frontend

WORKDIR /star-burger

COPY . .
RUN npm install -g n
RUN npm ci
EXPOSE 3000
RUN ./node_modules/.bin/parcel build bundles-src/index.js --dist-dir staticfiles/bundles --public-url="./"
