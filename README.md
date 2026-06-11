Spring Boot Docker App 🐳
A Spring Boot REST API containerized with Docker.

Tech Stack

Java 17
Spring Boot
Docker


Prerequisites
Make sure these are installed on your machine:

Docker Desktop
Java 17
Maven


Step 1 — Clone the Repository
git clone https://github.com/yourusername/your-repo-name.git
cd your-repo-name

Step 2 — Build the Docker Image
bashdocker build -t spring-boot-app .

Step 3 — Run the Container
bashdocker run -p 8080:8080 spring-boot-app
App will be running at: http://localhost:8080

Step 4 — Useful Docker Commands
bash# See running containers
docker ps

# See logs of your container
docker logs <container_id>

# Stop the container
docker stop <container_id>

# Remove the container
docker rm <container_id>

# Remove the image
docker rmi spring-boot-app

Step 5 — Push Image to Docker Hub
bash# Login to Docker Hub
docker login

# Tag your image with your Docker Hub username
docker tag spring-boot-app yourdockerhubusername/spring-boot-app:latest

# Push to Docker Hub
docker push yourdockerhubusername/spring-boot-app:latest
Image will be live at:
👉 https://hub.docker.com/r/yourdockerhubusername/spring-boot-app

Pull Image from Docker Hub
Anyone can run your app directly without cloning the code:
bashdocker pull yourdockerhubusername/spring-boot-app:latest
docker run -p 8080:8080 yourdockerhubusername/spring-boot-app:latest

Project Structure
spring-boot-app/
├── src/                    
├── pom.xml                 
├── Dockerfile              
└── README.md
