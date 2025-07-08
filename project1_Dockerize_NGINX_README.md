<h1 align="center">Dockerize NGINX with a Custom index.html page</h1>

<p align="center"><img src="https://github.com/user-attachments/assets/efd22002-794a-4fd7-89af-4bf5b8c2a356" alt="image1" /></p>

<h3>What is NGINX?</h3>
<p>NGINX is a fast and lightweight web server. It is commonly used to serve websites, handle high traffic, and act as a reverse proxy. It’s known for its speed and efficiency.</p>

<p>This project is great for beginners who want to learn how to use NGINX with Docker. You can easily customize and reuse it for your own projects.</p>
<p></p>
<b>Dockerfile and index.html file in working directory:</b>
Both the files are present in docker/project1_Dockerize_NGINX/ repo. Dockerfile to build an image and index.html to push customer webpage.
<p align="center"><img src="https://github.com/user-attachments/assets/4527e411-64b9-4bbb-a6d8-6cd251186777" alt="image1" /></p>
<b>Build Image:</b>
Image build process is here.</br>
Command: <b>docker build -t task1_nginx:latest .</b>
<p align="center"><img src="https://github.com/user-attachments/assets/f0816db6-dc08-485a-b4d0-df25df68c2d8" alt="image1" /></p>
<b>Verify Image:</b> Image is now built. We can verify by following command.</br>
Command: <b>docker images</b></br>
<p align="center"><img src="https://github.com/user-attachments/assets/0e7b8ed1-4c2c-4a27-ae14-2c753c2d2ec4" alt="image1" /></p>
<b>Run the container in detached mode:</b>
As we have created a docker image. Let’s Create a Container from that image.</br>
Command: <b>docker run -d -p 80:80 --name nginx task1_nginx</b>
<p align="center"><img src="https://github.com/user-attachments/assets/8cf88b36-504d-40cc-9c53-71a3bcb78d2e" alt="image1" /></p>
<b>Verify Container running:</b> Container is now created. We can verify by following command.</br>
Command: <b>docker ps</b></br>
<p align="center"><img src="https://github.com/user-attachments/assets/129db38c-667d-4449-967f-aa93d5918f0e" alt="image1" /></p>
<b>Executing inside the container and verify by using curl:</b></br>
Command: <b>docker exec -it nginx sh</b></br>
Command inside container: <b>curl localhost:80</b></br>
<p align="center"><img src="https://github.com/user-attachments/assets/46895208-6f1c-42c2-aac8-a3b471d75a08" alt="image1" /></p>
<b>Verify the page via Browser:</b>
<p align="center"><img src="https://github.com/user-attachments/assets/9e2d8509-9b45-42be-8ac2-bc7acc2901a7" alt="image1" /></p>
