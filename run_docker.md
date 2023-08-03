# How to Start with Docker Practically

## 1. Install Docker on Your Machine
Make sure you have Docker installed on your local machine. If you haven't installed it yet, follow the official Docker installation guide for your operating system.

## 2. Pull Docker Image from Docker Hub
You can choose any image from Docker Hub. For example, you can pull the following images:
- PostgreSQL: `docker pull postgres`
- MySQL: `docker pull mysql`
- Custom App: `docker pull sohit28/apps:v1.0`

Replace `sohit28/apps:v1.0` with the desired image name and version if you want to pull a specific custom app image.

## 3. View Docker Images
After pulling the image, you can view the list of available images by running the following command:
```bash
docker images
```

## 4. Run Docker Container
Now, it's time to run the Docker image you pulled. Use the following command to run the container:
```bash
docker run -d -p 8090:8000 sohit28/apps:v1.0
```
Replace `sohit28/apps:v1.0` with the actual image name and version if you pulled a custom app image.

## 5. Check Running Containers
To verify that the container is running, use the following command:
```bash
docker ps
```

If everything went well, you should see the container `sohit28/apps:v1.0` running in the list.

## 6. Test in Your Local Machine
Congratulations! You have successfully set up and tested the Docker container on your local machine. You can now access the application hosted by the container on `localhost:8090` (if the exposed port is `8000` inside the container).

Happy Dockerizing! 🐳
