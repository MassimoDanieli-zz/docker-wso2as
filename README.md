docker-wso2as
===================

Docker image to install and run WS02 Application Server . 
The WS02 Application Server brings together best of breed open source technologies for Web Applications (i.e. Apache Tomcat), Web Services (i.e. Apache Axis2), RESTful services (i.e. JAX-RS) with WSO2’s open source management, monitoring, clustering, and logging extensions.
It uses the [dockerfile/java](https://index.docker.io/u/dockerfile/java/) as its base image.


The dockerfile will:

* Use `wget` to pull the Application Server 5.2.1 zip file from WS02 web site into the container `/opt` folder.
* Install `zip`.
* Unzip the Application Server 5.2.1 zip file.
* Remove the AS zip.
* Expose the container port `9443`.
* Set the AS  `wso2server.sh` start-up script as the container start-up command.

### Usage

* To pull: `docker pull massimodanieli/wso2as`
* To build: `docker build --rm -t your_image_name github.com/massimodanieli/docker-wso2as`
* To run: `docker run --rm --name your_container_name -p 9443:9443 your_image_name`
* To access Application Server web admin console, navigate to `https://localhost:9443`

