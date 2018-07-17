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

Now move into the folder created by the clone and run the folowing command to build the docker image

```
docker build -t <image-tag> .
```
You can run the command below to list all images, you can use this to check if the image was created with the correct tag

```
docker images
```
When you know the images has been created you can run the application using the image, in the following code I will map the application to port 80. We use the same image tag as when we created the image with the 'docker build' command

```
docker run -p 80:80 <image-tag>
```
The application should now be running and accessible on (http://localhost:80)
