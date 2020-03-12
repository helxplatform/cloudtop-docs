Usage
*****

CloudTop is provided only as a docker image.  The images are stored in dockerhub (https://hub.docker.com/) and are downloaded with the normal mechanisms in docker run, docker-compose and kubernetes. 

*Tags*

* heliumdatastage/cloudtop:ohif  This docker file includes both the CloudTop and the Google Health enabled version of the OHIF dicom viewer.

*Ports*

* 8080 This is the native port for the web connection to CloudTop
* 3000 (OHIF version only) This is the port for the OHIF web application

*Environment Variables*

* USER_NAME The name to use to log in to the CloudTop instance. This user is created in the running docker image.
* USER_HOME The home directory for the created user.  CloudTop is running a Linux variant so this should be set to /home/USER_NAME.
* VNC_PW The password to use to log in to the CloudTop instance.
* CLIENT_ID (OHIF version only) The Google API Client Identifier token created using the Google tools.

