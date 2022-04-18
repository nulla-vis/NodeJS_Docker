### My process to build a template for NodeJS + Docker application

### Docker with NodeJS

### Configuration
 + To build the image, run command: `docker build -t <image-name> .`.
 + To check image list run commbad: `docker image ls`.
   For removing an image, from the image list, copy the image id and remove it with command: `docker image rm <imageId>`.

### Running image / manual configration
 + make sure to set .env file on root.
 + To run the image, simply run with command: `docker run -v <pathToFolderOnLocalMachine>:<pathToFolderOnContainer>:ro -v /app/node_modules --env-file ./.env -p <port-to-access>:<port-inside-docker> -d --name <image-alias> <image-name>`.
  On windows path can be change to %cd%:, on macOs/Linux use $(pwd).
 + To check running image, run command: `docker ps`.

### Entering/login to a specific image
 + Run command: `docker exec -it <image-name> bash`. To exit just type : `exit`.
 + To check environtment variables run command on image bash: `printenv`.

### Easy running image
 + to run the container easily, simply run: `docker-compose up -d` on root project.
  + To take it down, run command: `docker-compose down -v`.