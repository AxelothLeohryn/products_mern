# Product-MERN-Docker

Application made with ReactJS + ExpressJS + MongoB

You must have Docker and docker-compose Installed in your System !

### How to run the App :

#### Development

Run the app using:

`$ docker-compose -f docker-compose-dev.yml up `

or

`$ docker-compose up -d`

Above command will start the services on (-d) detach mode (similar like running the app in background)

Then you can check the status of the containers by running:

`$ docker ps`

visit server or client : http://localhost:8080

To check the status of the running containers :

`docker-compose ps`


#### Production

To deploy in AWS EC2

Run the app using:

`$ docker-compose up -d --build --remove-orphans`

or

`$ docker-compose up -d`

Above command will start the services on (-d) detach mode (similar like running the app in background)

Then you can check the status of the containers by running:

`$ docker ps`

visit server or client : `your_aws_ip:80`

To check the status of the running containers :

`docker-compose ps`


# Execute MERN app

## Launch client + server
```javascript
cd client
//client
npm ci

cd ..
// server
npm ci 

//Preload data MongoDB - seeder
npm run feed_db

// run MERN app
npm run dev
```

# API REST products - Express + MongoDB

API REST Node.js, Express, MongoDB (local) or MongoDB Atlas cloud. 
Some clarifications about backend

## Instalation
```javascript
npm i 
npm i --save-dev nodemon
```

## Preload data MongoDB - seeder

```javascript
npm run feed_db
```

## Start backend for development
```javascript
  npm run server
```

## Start backend for production
```javascript
  npm start
```
## Connect with MongoDB Atlas
Rename `.env.example` to `.env` and add your URL mongoDB atlas
```
DB_URL_ATLAS=
```
## Endpoints

- GET products. Pagination from backend

```javascript
GET http://localhost:3000/api/products
GET http://localhost:3000/api/products?page=1&limit=2
GET http://localhost:3000/api/products?page=2&limit=3

```

- POST new product
```javascript
POST http://localhost:3000/api/products

Request:
{
"title": "Bocadillo Lomo Queso - Rocafría",
"price": 4.20,
"description": "El mejor bocadillo del barrio",
"image": "https://babelcafeloungebar.com/wp-content/uploads/2021/02/bocadillo-lomo-queso-babel.jpg"
}

Response:
{
"message": "Producto Bocadillo Lomo Queso - Rocafría guardado en el sistema con ID: 632f9a5236a3262c5b1b417a"
}
```

