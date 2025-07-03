<h1>📦 Dockerfile Overview</h1>

A Dockerfile is a plain text file that defines a sequence of instructions for Docker to follow in order to build an image. It’s similar to a cookbook recipe—just like we follow steps to cook a dish, Docker follows these instructions to create image layers.

Once the image is built, it can be shipped and deployed anywhere, and containers can be created from that image on any environment that supports Docker.

The process of Dockerizing an application typically involves:</br>
1- Creating a Dockerfile.</br>
2- Building the Docker image from that file.</br>
3- Running the application inside a Docker container.</br>

This approach ensures consistency, portability, and simplified deployment across development, testing, and production environments.

<h1>🔁 Lifecycle of a Dockerfile</h1>
The lifecycle of a Dockerfile typically involves the following stages:

<h3>1️⃣ Create the Dockerfile</h3>
A text file must be created name Dockerfile with capital D and no space:</br>
</br>
- Which base image to use</br>
- Commands to install dependencies</br>
- Files to copy</br>
- Ports to expose</br>
- The default command to run

<h3>2️⃣ Build the Docker Image</h3>
You convert the Dockerfile into a Docker image using:</br>
<b>docker build -t my-app-image .</b>

<h3>3️⃣ Verify the Image</h3>
We can list and inspect images using:</br>
<b>docker images</b>
<b>docker image inspect my-app-image</b>

<h3>4️⃣ Run a Container</h3>
We can launch a container using the built image:</br>
<b>docker run -d -p 80:80 --name my-container my-app-image</b></br>
The container is an isolated runtime environment for the app.</br>
Any changes inside a container are not saved to the image unless committed.

<h3>5️⃣ Test and Debug</h3>
We can enter the running container to debug or test:</br>
<b>docker exec -it my-container bash</b>

<h3>6️⃣ Stop and Remove Containers</h3>
<b>docker stop my-container</b>
<b>docker rm my-container</b>

<h3>7️⃣ Push the Image to a Registry</h3>
We can upload the image to Docker Hub or any other registry:</br>
<b>docker tag my-app-image username/my-app-image:latest</b></br>
<b>docker push username/my-app-image</b>

<h3>8️⃣ Deploy the Image Anywhere</h3>
Use the pushed image to deploy in:
Other Docker hosts
Cloud platforms

<h3>📌 Summary</h3>
<b>Dockerfile ➡️ docker build ➡️ Docker Image ➡️ docker run ➡️ Container</b>
