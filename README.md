## Product-MERN-Docker

You must have Docker  and docker-compose Installed in your System !

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

