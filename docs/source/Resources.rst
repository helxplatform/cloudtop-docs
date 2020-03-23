Resources
*********

CloudTop images are stored in dockerhub (https://hub.docker.com/) and are downloaded with the normal mechanisms in docker run, docker-compose and kubernetes. Also available are the Github repositories and docker files used to make the images. Please see the docker files for cloudtop-ohif and cloudtop-imagej-napari for examples of how to create your own CloudTop based docker images.

*CloudTop Docker Tags*

* cloudTop: heliumdatastage/cloudtop:latest 
* cloudTop-ohif: heliumdatastage/cloudtop-ohif:latest
* cloudtop-imagej-napari: heliumdatastage/cloudtop-imagej-napari:latest

*CloudTop GitHub Repositories*

* cloudTop: https://hub.docker.com/repository/docker/heliumdatastage/cloudtop
* cloudTop-ohif: https://hub.docker.com/repository/docker/heliumdatastage/cloudtop-ohif
* cloudtop-imagej-napari:  https://hub.docker.com/repository/docker/heliumdatastage/cloudtop-image-napari

*Direct links to docker files*

* cloudTop: https://github.com/helxplatform/cloudtop/blob/master/Dockerfile
* cloudTop-ohif: https://github.com/helxplatform/cloudtop-ohif/blob/master/Dockerfile
* cloudtop-imagej-napari: https://github.com/helxplatform/cloudtop-imagej-napari/blob/master/Dockerfile

*S6 Usage and Documentation*

CloudTop and it's derived products use the S6 system for system intialization and process management. CloudTop uses S6 for the following:

* System initialization: Needed processes, for example the nginx web server or tomcat servlet container can be started at the time the docker container is initialized.  The S6 system will monitor these processes and restart them as needed.

* User/desktop customization: The initialization scripts can also execute shell scripts for user customization. For example, the cloudtop-imagej-napari script copies several desktop launcher files into the Desktop directory of the user. This is needed because, for security reasons, the user account is created as part of the container initialization.

The cloudtop-ohif and cloudtop-imagej-napari repos and docker files are good examples of how to extend the CloudTop base image using these S6 capabilities. For documentaion on the S6 system see:

https://skarnet.org/software/s6/
