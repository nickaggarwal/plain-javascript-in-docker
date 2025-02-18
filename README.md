# plain-javascript-in-docker
JavaScript + HTML to render Hello Page 


PROJECT START STEPS:

    Pre-requisites:
    1. Install http-server module (https://www.npmjs.com/package/http-server).

    Steps:
    1. To run this application, do the following:
        1.a. Go to the project root directory.
        1.b. Run the following command(s) in the terminal/command line:    
            - http-server ./ -p <port_number> -a 0.0.0.0
    
    2. Go to http://localhost:<port_number>/ in your browser to view it.


DOCKER START STEPS:

    Pre-requisites:
    1. Docker is installed (http://console.codejudge.io/setup)

    Steps:
    1. Build the docker image:
        1.a. Go to the project root directory.
        1.b. Run the following command(s) in the terminal/command line:
            - docker build -t cj-app .

    2. Run the image in a container (Make sure port 4200 is available):        
        2.a. Run the following command(s) in the terminal/command line:
            - docker run -i -p4200:4200 cj-app
        2.b. Check the logs for any errors. 

    3. Go to http://localhost:4200 in your browser to view it.

DOCKER STOP STEPS:

    Steps:
    1. Run the following commands:
        - docker ps
    2. Copy the container id and run the below command:
        - docker stop <container_id> 
        - docker system prune

DOCKER LOGS:

    Steps:
    1. Run the following commans(s):
        - docker ps
    2. Copy the container id and run the below command:
        - docker logs <container_id>

DOCKER REMOVE CONTAINER:

    Steps:
    1. Run the following command(s):
        - docker ps
    2. Copy the container id and run the below command:
        - docker rm <container_id>
        - docker system prune

DOCKER REMOVE IMAGE:

    Steps:
    1. Run the following command(s):
        - docker ps
    2. Copy the image id and run the below command:
        - docker rmi <image_id>
        - docker system prune
