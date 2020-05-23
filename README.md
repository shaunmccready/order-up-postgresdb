# Order-up! - PostgreSQL database for Java API

* _Java backend Api repository is located at (https://github.com/shaunmccready/order-up-api)_


***
***

### Tech stack used:
- [PostgreSQL v.11](https://www.postgresql.org/docs/11/index.html)
- [Docker CE](https://www.docker.com/why-docker)


### Purpose for the App
For guests of parties to indicate to the hosts what they are eating, drinking, etc. 
You place your order and the chef/bartender can prepare your item and call you when ready


## Installation

You will need to define the following environment variables inside your docker container:

- POSTGRES_PASSWORD (password for the superuser of the DB)
- POSTGRES_USER (user name for the superuser of the DB)
- POSTGRES_DB (name of the data base)


You will also want to expose the containers port of 5432 externally. Also setup a volume

While inside the folder where the `Dockerfile` is located (where you cloned this repository) 
run: `docker build -t name_you_want_for_image .`  <-- (thats a space and period to say current dir)

After the image is built, you run the following command (substituting your names) to create and start 
the docker container:

 `docker run --rm --name your_container_name -p 5432:5432 -v /location_of_your_host_folder:/var/lib/postgresql/data name_of_your_image`

