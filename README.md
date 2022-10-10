## Creating Docker images.

### Initial steps:
 1. Download and install Docker windows.
 2. Register and login to Coder hub.
  - All our Docker repositories are in Docker hub.


### step 1: <br />
 create a folder with all necessary code. <br />
 
### step 2:<br />
 create requirements.txt with the list of neccesary libraries.<br />
 
### step 3: <br />
 Add Dockerfile in the folder.<br />
 
 		 FROM python:3.7    //it copies this docker image from docker hub. <br />
		 COPY .  /app              //copy the code in local folder to app folder in docker image <br />
		 WORKDIR /app        //keeping app folder as working directory <br />
		 RUN pip install -r requirements.txt           //install all the required libraries present in requirements.txt file <br />
   		 CMD ["python", "app.py"]                          //command to run the file.    Python app.py <br /> 

 

### commands to create Docker image <br />

<em><strong> In local machine: </strong></em> <br />

- docker build -t dockerimagename .<br />
- docker images     <br />     
 	- gives the list of docker images <br />
- docker run -d -p hostport:containerport containername <br />

<em><strong> To push the Docker image to Docker hub: </strong></em> <br />

- docker build -t username/dockerimage . <br />
- docker push username/dockerimage:latest <br />

<em><strong> Few usful Docker Commands </strong></em> <br />
 
- docker images    <br />          
 	- lists all the docker images <br />
- docker ps         <br />         
	- lists the running containers <br />
- docker rmi imageID   <br />      
	- deletes image <br /> 
- docker rm -f containerID    <br />
	- forcefully deletes the container. <br />
	
	
<em><strong>To pull this topic from my docker repository</strong></em> <br />
 
- docker pull sowjanyasadashiva/hello-world    <br />          
- docker run -d -p 5000:5000 hello-world         <br />         
	
 
 
 
 
 

 
