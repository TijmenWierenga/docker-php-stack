# PHP-Apache Development Stack
A lightweight development environment for developing PHP packages. Made by Tijmen Wierenga.
The current setup runs PHP 7.1 and Apache 2.

## Prerequisites
In order to run this environment you need to have both *Docker* and *Docker-Compose* installed. 

## Installation
Simply clone the repository to your local machine.

>For the following instructions: make sure you are in the root directory of the cloned repository

Next, copy the contents of the `.env.dist` file to `.env` and change the environment variables to your preferences:
``` bash
cp .env.dist > .env
```

Then start the container with *docker-compose*:
``` bash
docker-compose up -d
```

Once the container is running, you can enter it with a simple command:
``` bash
bin/bash
```

Now make something great!
