# Radix-HTML-scenario1
This is a simple html page dockerised using nginx. No external dependencies. No back end dependencies. No storage. No secrets. Static/Dynamic web page 

## Getting started
Follow these instructions to get a copy of the project on your local machine

### Prerequisites
To run this project localy you need to install Docker.
* Get Docker - [Docker](https://docs.docker.com/install/)

### Run the app
First you need to clone this repository using git clone

```
git clone <repo-url>
```

Now move into the folder created by the 'git clone' command and run the following command to build the docker image with a custom image tag

```
docker build -t <image-tag> .
```
You can run the command below to list all images, use this to check if the image was created with the correct tag

```
docker images
```
When you know the image has been created you can run the application using the image, in the following code I will map the application to port 80. We use the same image tag as when we created the image with the 'docker build' command

```
docker run -p 80:80 <image-tag>
```
The application should now be running in a container and accessible on http://localhost:80, you can also view all running container by opening a new terminal window and then enter the following command

```
docker container ps
```
