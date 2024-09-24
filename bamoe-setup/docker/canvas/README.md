# Installing BAMOE Canvas with Docker Compose

BAMOE Canvas and its related services can be run on a single machine using `Docker Compose` for BAMOE Canvas.

## Prerequisites
You need `Docker Compose` to run the BAMOE Canvas. Since Docker Desktop is no longer supported by IBM, the easiest way is to use Rancher Desktop.  Click [here](https://docs.rancherdesktop.io/getting-started/installation/) in order to get instructions on how to install Rancher Desktop in Docker mode.  

## Run
In a terminal, navigate to the folder where you downloaded the BAMOE Canvas Docker Compose YAML file, and run the command: 

`docker compose up`

For BAMOE Canvas, you can access this by default at [IBM Canvas](http://localhost:9090), which is configured in the compose yaml with various settings. These can be further customized, for documentation on it refer to the [Quay Image Repository](https://quay.io/repository/bamoe/canvas) and the [Product Documentation](https://www.ibm.com/docs/en/ibamoe/9.0.0).
