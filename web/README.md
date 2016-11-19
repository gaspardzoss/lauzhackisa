## Install
    
    # Create the docker-machine if needed
    docker-machine create -d virtualbox dev;

    # Find its ip
    docker-machine ip dev

    # Build the containers 
    docker-compose build

    # Run the containers
    docker-compose up


## Clean Docker

    docker rm -f `docker ps --no-trunc -aq`
    docker rmi -f `docker images | awk '{ print $3; }'`


## Connect to Docker Container

    docker exec -it <containerIdOrName> bash