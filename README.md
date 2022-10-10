Creating Docker images.

initial steps:
 1. Download and install Docker windows.
 2. Register and login to Coder hub.
  - All our Docker repositories are in Docker hub.


step 1:
 create a folder with all necessary code.
step 2:
 create requirements.txt with the list of neccesary libraries.
step 3: 
 Add Dockerfile in the folder.
 		FROM python:3.7    //it copies this docker image from docker hub.
		 COPY .  /app              //copy the code in local folder to app folder in docker image (.  Means all the files in folder)
		 WORKDIR /app        //keeping app folder as working directory
		 RUN pip install -r requirements.txt           //install all the required libraries present in requirements.txt file
   CMD ["python", "app.py"]                          //command to run the file.    Python app.py

 

commands to create Docker image

In local machine: 

>> docker build -t <dockerimagename> .
>> docker images  //gives the list of docker images
>> docker run -d -p <hostport>:<containerport> <containername>

To push the Docker image to Docker hub:

>> docker build -t <username>/<dockerimage> .
>> docker push <username>/<dockerimage>:latest

Few usful Docker Commands
 
>> docker images //lists all the docker images
>> docker ps  //lists the running containers
>> docker rmi <imageID>  //deletes image
>> docker rm -f <containerID>  //forcefully deletes the container.
 
 
 
 
 

 
