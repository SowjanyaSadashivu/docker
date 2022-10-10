##Creating Docker images.

**Initial steps:
 1. Download and install Docker windows.
 2. Register and login to Coder hub.
  - All our Docker repositories are in Docker hub.


step 1: <br />
 create a folder with all necessary code. <br />
step 2:<br />
 create requirements.txt with the list of neccesary libraries.<br />
step 3: <br />
 Add Dockerfile in the folder.<br />
 		 *FROM python:3.7    //it copies this docker image from docker hub. *<br />
		 *COPY .  /app              //copy the code in local folder to app folder in docker image* <br />
		 *WORKDIR /app        //keeping app folder as working directory* <br />
		 *RUN pip install -r requirements.txt           //install all the required libraries present in requirements.txt file* <br />
   		 *CMD ["python", "app.py"]                          //command to run the file.    Python app.py *<br /> 

 

commands to create Docker image <br />

In local machine: <br />

- docker build -t <dockerimagename> .<br />
- docker images  //gives the list of docker images <br />
- docker run -d -p <hostport>:<containerport> <containername> <br />

To push the Docker image to Docker hub: <br />

- docker build -t <username>/<dockerimage> . <br />
- docker push <username>/<dockerimage>:latest <br />

Few usful Docker Commands <br />
 
- docker images //lists all the docker images <br />
- docker ps  //lists the running containers <br />
- docker rmi <imageID>  //deletes image <br /> 
- docker rm -f <containerID>  //forcefully deletes the container. <br />
 
 
 
 
 

 
