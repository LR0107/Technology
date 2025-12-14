## Docker (Windows)

### Build Docker Image

Open PowerShell or CMD and navigate to your project directory:

`docker build -t myapp .`

### Run Container

`docker run -p 5000:5000 myapp`

### Dockerfile

Package configuration file: `Dockerfile` (no file extension)

### Other Common Commands

#### Pull an Image

`docker pull nginx`

#### List Images

`docker images`

#### Stop a Container

`docker stop myapp`
