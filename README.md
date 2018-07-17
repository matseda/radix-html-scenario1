# Radix-HTML-scenario1
This is a simple html page containerized using docker. No external dependencies, back end dependencies, storage or secrets.

## Getting started
Follow these instructions to get a copy of the project on your local machine

### Prerequisites
To run this project localy you need to install Docker.
* Get Docker - [Docker](https://docs.docker.com/install/)

### Run localy
First you need to get a local copy of this repository, this could be done using git clone

```
git clone <repo-url>
```

Now move into the folder created by the 'git clone' command and run the following command to build the docker image with a custom image tag, in the example we use 'radixhtml:1.0' which will result in the image getting the repository name 'radixhtml' and the tag '1.0'

```
docker build -t <image-tag> .

##Example 
docker build -t radixhtml:1.0 .
```
Run the application using the image, in the following code I will map the application to port 80. We use the same image tag as when we created the image with the 'docker build' command

```
docker run -p 80:80 <image-tag>
```
The application should now be running in a container and accessible on http://localhost:80, when you want the container and the application to stop running you simply go into the terminal window where you executed the 'docker run' command and press Ctrl+C.

### Troubleshooting

You can run the command below to list all images, use this to check if an image was created 

```
docker images
```

You can view all running container by running the following command, use this to check if your application is running 

```
docker container ps
```

## Deployment

To deploy this app on the radix web console follow the steps described in the [Radix Wiki](https://radix-wiki.azurewebsites.net/doku.php/appdeveloper/gettingstarted)

## Built With
* [Docker](https://docs.docker.com/) - Containerizing the app

## Authors
* **Mats Davidsen**
