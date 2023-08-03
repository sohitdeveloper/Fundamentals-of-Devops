# How to Start with Docker Practically?

To deploy an application using Docker, follow these steps:

1. Create Your Application and Add a Dockerfile

In the root directory of your application, create a `Dockerfile`. This file contains instructions necessary for running the application in any machine. For instance, if you have a backend application running on the Node.js environment, your `Dockerfile` may look like this:

```Dockerfile
# Use the official Node.js image
FROM node:14

# Set/create the working directory inside the container
WORKDIR /app

# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./

# Install dependencies
RUN npm install

# Copy the rest of the application code to the working directory
COPY . ./

# Expose the port that your Express application listens on
EXPOSE 8000

# Start the Node.js application
CMD [ "node", "app.js" ]
```

2. Build the Docker Image

To build the Docker image from the `Dockerfile`, run the following command:

```bash
docker build -t your-image-name .
```

Replace `your-image-name` with a suitable name for your Docker image.

3. View Docker Images

After building the image, you can view the list of available images by running the following command:

```bash
docker images
```

4. Authenticate with Docker Hub

Before pushing your image to Docker Hub, you need to be authenticated. Run the following command and enter your Docker Hub credentials when prompted:

```bash
docker login
```

5. Tag and Push the Docker Image

Next, tag your Docker image with your Docker Hub username and desired version:

```bash
docker tag your-image-name sohit28/myapp:v1.0
```

Replace `your-image-name` with the name you used while building the image, and `sohit28/myapp:v1.0` with your Docker Hub username and the version you want.

Now, push the tagged image to Docker Hub:

```bash
docker push sohit28/myapp:v1.0
```

6. Confirm the Image Push

After successfully pushing the image, you can visit your Docker Hub account's repository page to see the newly published image.

Congratulations! You have now successfully built, tagged, and pushed your Docker image to Docker Hub, making it available for others to use. Happy Dockerizing! 🐳
