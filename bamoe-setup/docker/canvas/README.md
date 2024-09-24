# Installing BAMOE Canvas with Docker Compose

BAMOE Canvas and its related services can be run on a single machine using `Docker Compose` for BAMOE Canvas.

## Prerequisites
You need `Docker Compose` to run the BAMOE Canvas. Since Docker Desktop is no longer supported by IBM, the easiest way is to use Rancher Desktop.  Click [here](https://docs.rancherdesktop.io/getting-started/installation/) in order to get instructions on how to install Rancher Desktop in Docker mode.  

## Run
In a terminal, navigate to the `bamoe-setup/docker/canvas` folder and run the following command: 

`docker compose up`

## Canvas
Once the container image is up and running, you can access `BAMOE Canvas` [here](http://localhost:9090).  