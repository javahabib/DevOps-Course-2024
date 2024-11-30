# 🚀 NGINX Docker Web App

Welcome to the **NGINX Docker Web App** repository! This is a simple web application that uses **Docker** to run an **Nginx** server which serves a static HTML page. The purpose of this project is to demonstrate a basic cloud and DevOps setup.

## 📝 Project Overview

This project uses the following:

- **Nginx**: Lightweight, high-performance web server.
- **Docker**: Containerizes the application to ensure it runs consistently across different environments.

### 🗂️ Project Structure

The project consists of the following files:

- `**index.html**`: A simple HTML file containing the webpage content.
- `**Dockerfile**`: A configuration file for building the Docker image and running the Nginx server.

---

## 🛠️ Setup & Installation

Follow these steps to run the application locally using Docker.

### 1️⃣ Clone the Repository
  ```bash
   git clone <[repository-url](https://github.com/zaibunnisaq/DevOps-Course-2024/Docker_NGINX-Web-App)>
   cd <[repository-directory](https://github.com/zaibunnisaq/DevOps-Course-2024)>
```

###2️⃣ Build the Docker Image
In the project directory, build the Docker image:
```bash
docker build -t nginx-webapp .
```

3️⃣ Run the Docker Container
Once the image is built, run the container:
```bash
docker run -d -p 8080:80 nginx-webapp
```

4️⃣ View the Web App
Now, open your browser and visit http://localhost:8080 to see the webpage being served

🌍 Deploy to AWS EC2
Follow these steps to deploy your NGINX Docker web app on an AWS EC2 instance.

1️⃣ Launch an EC2 Instance
Go to the AWS EC2 Dashboard.
Click Launch Instance.
Select an Amazon Machine Image (AMI) such as Ubuntu.
Choose an instance type (e.g., t2.micro for free-tier).
Configure the instance and add storage if needed.
Create a new key pair or use an existing one for SSH access.

2️⃣ SSH into the EC2 Instance
After the instance is running, SSH into it using the following command:
```bash
ssh -i path/to/your-key.pem ubuntu@<EC2_PUBLIC_IP>
```

3️⃣ Install Docker on EC2
```bash
sudo apt-get update
sudo apt-get install -y docker.io
```
Enable and start Docker:
```bash
sudo systemctl enable docker
sudo systemctl start docker
```

4️⃣ Build and Run the Docker Container on EC2
```bash
docker build -t nginx-webapp .
docker run -d -p 80:80 nginx-webapp
```

5️⃣ Access the Web App
Open your browser and visit the public IP of your EC2 instance

🔧 How It Works
index.html: This file contains a basic webpage with the title "Cloud and DevOps Assignment" and additional details related to your assignment.

Dockerfile:
Uses the official nginx:alpine base image.
Copies index.html to Nginx's default HTML directory.
Exposes port 80 to make the page accessible from the outside.

💻 Technologies Used
Docker: For containerizing the web application.
Nginx: Web server to serve the static HTML content.
HTML: Simple web page displaying assignment details.
AWS EC2: Deployed the application in the cloud.

