# Microsoft Technology company-Cloud Native projects
## _My Projects List :_
## - 1/ Build a containerized web application with docker
![caption](https://github.com/Mqueen15/Cloud-Native-Engineer/blob/main/Microsoft%20Technology%20company/Build%20a%20containerized%20web%20application%20with%20docker.gif?raw=true)

Building and running your own Docker images is to take an existing image from Docker Hub and run it locally on your computer. Here the steps for a good starting :

- Pull and run a sample application from Docker Hub
- Examine the container in the local Docker registry
- Remove the container and image from the local registry

## Steps

- Pull the ASP.NET Sample app image from the Docker Hub registry. This image contains a sample web app developed by Microsoft. It's based on the default ASP.NET template available in Visual Studio.
- Verify that the image has been stored locally.
- Start the sample app. Specify the -d flag to run it as a background, non-interactive app. Use the -p flag to map port 80 in the container that is created to port 8080 locally, to avoid conflicts with any web apps already running on your computer. The command will respond with a lengthy hexadecimal identifier for the instance.
- Open a web browser, and navigate to the page for the sample web app at http://localhost:8080. 


## Tools, Environnement & Dependencies :

This project uses these tools to work properly:

- Docker and DockerHub
- Powershell last version

