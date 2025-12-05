# Docker (Windows)

1. Build the Docker image: Open PowerShell or CMD and navigate to your project directory  
   `docker build -t myapp .`
2. Run the container  
   `docker run -p 5000:5000 myapp`

Packaging: Dockerfile (no file extension)

Other commands  
Pull an image: `docker pull nginx`  
View images: `docker images`  
Stop container: `docker stop myapp`


