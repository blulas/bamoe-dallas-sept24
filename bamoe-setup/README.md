# Installing IBM Business Automation Manager Open Editions on a Local Workstation

## Requirements for Local Machine Setup
The following instructions are helpful in setting up your local environment in order to do BAMOE development.  All functions of BAMOE are available from the developer workstation, including web-based tools and consoles.

- **JDK 17** (https://developer.ibm.com/languages/java/semeru-runtimes/downloads/), prefer the IBM Semeru release of JDK, but any OpenJDK will do
- **GIT Command Line Interface** (https://git-scm.com/downloads), plus you are free to install any GIT related extensions or simply use the command line tools
- **Maven Command Line Interface** (https://maven.apache.org/install.html), used for builds and deployments of BAMOE libraries, plus you are free to install any Maven related extensions or simply use command line tools.
- **VS Code IDE** (https://code.visualstudio.com/download), and install the following extensions from the VS Code Marketplace:
BAMOE Developer Tools, this is the set of editors for DMN, BPMN, and PMML that developers use to create their visual models in the IDE
Drools (by Jim Moody), this is a third-party editor which does simple syntax highlighting of the Drools Rule Language (DRL) files

## Running Container Images Locally
There are several pre-built container images which assist the developer.  These images require a container management system, such as **Docker**, **PodMan**, or **Rancher Desktop**.  Most BAMOE technologists use **Rancher Desktop**, which can be run in “docker” mode, and we can supply a startup repository that installs Canvas and other images into your Rancher installation.  If you plan to install the container images on your laptop, we will also guide you through this, but here are the instructions if you want to get ahead.

- **BAMOE Canvas** (_optional_), which is the next generation of web-based modeling tools, can be installed either on your local workstation or via a shared server   Canvas is available as a published container image at:  https://quay.io/repository/bamoe/canvas.  There are two other container images necessary to run Canvas, the **Extended Services**:  https://quay.io/repository/bamoe/extended-services, and the **CORS Proxy**: https://quay.io/repository/bamoe/cors-proxy.

- **BAMOE Maven Repository**, is a on-premise container image that provides local access to the product’s Maven libraries, which are the building blocks of BAMOE projects.  To build a BAMOE project, you must have access to either the container image or create a local off-line Maven repository, possibly in an Artifactory instance or some other sort of Maven server.  The BAMOE installation files include an off-line version of the Maven libraries, but it is recommended to use the container image, as IBM re-spins their images every 30 days to combat CVE’s.  The image is available at:  https://quay.io/repository/bamoe/maven-repository.

- **Management Consoles** are a set of cloud-native consoles used to administer stateful business processes.
TBD...