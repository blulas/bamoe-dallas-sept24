# Installing BAMOE Maven Repository Container Image

With IBM Business Automation Manager Open Editions v9.1 aligning with its previous version BAMOE v8 in the downstream build model, the artifacts are no longer available in Maven Central. The artifacts are shipped as part of the product as a Container Image and Maven Repository inside the compressed file in a consumable format.

## Prerequisites
You need `Docker Compose` to run the BAMOE Maven container image. Since Docker Desktop is no longer supported by IBM, the easiest way is to use Rancher Desktop.  Click [here](https://docs.rancherdesktop.io/getting-started/installation/) in order to get instructions on how to install Rancher Desktop in Docker mode.  

## Pull the Container Image
In a terminal, navigate to the `bamoe-setup/maven` folder and run the following command: 

```sh
docker pull quay.io/bamoe/maven-repository:9.1.0-ibm-0001
```

## Run
```sh
docker run -d -p <PORT>:80 quay.io/bamoe/maven-repository:9.1.0-ibm-0001
```

_Replace PORT with whatever port you want the container to be mapped to on your host._

## Maven Settings
Copy the supplied [Maven Settings](settings.xml) file into the `~/.m2/` directory, assuming you installed using port 8088, or replace the port with the actual port you installed the image to.