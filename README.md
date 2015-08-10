docker-wso2as
===================

Docker image to install and run WSO2 Application Server . It uses the [dockerfile/java](https://index.docker.io/u/dockerfile/java/) as its base image.


The dockerfile will:

* Use `wget` to pull the Application Server ZIP from WS02 web site into the container `/opt` folder.
* Install `zip`.
* Unzip the AS ZIP.
* Remove the AS ZIP.
* Expose the container port `9443`.
* Set the AS  `wso2server.sh` start-up script as the container start-up command.

### Usage
* To pull: `docker pull massimodanieli/wso2as`
* To build: `docker build --rm -t your_image_name github.com/massimodanieli/docker-wso2as`
* To run: `docker run --rm --name your_container_name -p 9443:9443 your_image_name`
* To access Application Server web admin console, navigate to `https://localhost:9443`

