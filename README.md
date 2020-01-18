This app is built for dockerizing NodeJS application.
For this app to run, docker needs tobe installed.

Then run
docker build -t <your username>/node-web-app .

Your image will now be listed by Docker:
To view:
docker images

Running your image with -d runs the container in detached mode, leaving the container running in the background. The -p flag redirects a public port to a private port inside the container. Run the image you previously built:

docker run -p 49160:8080 -d <your username>/node-web-app

# Get container ID

docker ps

If you need to go inside the container you can use the exec command:

# Enter the container

docker exec -it <container id> /bin/bash

Now go to localhost:49160, your app response will be displayed as "Hello World"
