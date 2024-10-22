# Nginx Web Server

This project sets up a simple Nginx web server using Docker to serve a static HTML page. It is designed for quick deployment and easy customization.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Customization](#customization)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

## Overview

This project demonstrates how to create and run a lightweight web server using Nginx in a Docker container. It serves a static HTML page with a simple message.

## Prerequisites

Before you begin, ensure you have the following installed:

- **Docker**: You can download and install Docker from [Docker's official website](https://www.docker.com/get-started).

## Installation

Follow these steps to set up the project on your local machine:

1. **Clone the repository**:
   Open your terminal and run:
   ```bash
   git clone https://github.com/Vikashchaurasiya07/Nginx-Web-server.git
   cd Nginx-Web-server
Build the Docker image: Create the Docker image from the Dockerfile:
bash
Copy code
docker build -t my-nginx .
Usage
Run the Docker container: Start the container in detached mode, mapping port 8080 on your host to port 80 in the container:

bash
Copy code
docker run --name my-nginx-container -d -p 8080:80 my-nginx
Access the web server: Open your web browser and navigate to:

arduino
Copy code
http://localhost:8080
You should see the message "Hello, Nginx!".

How It Works
Dockerfile: This project includes a Dockerfile that specifies the base image as the official Nginx image from Docker Hub.
HTML Content: The static HTML file index.html is copied to the appropriate directory within the container where Nginx serves files.
Port Mapping: The container maps port 8080 on your local machine to port 80 in the container, allowing you to access the web server easily.
Customization
You can customize the web page by editing the index.html file:

Open index.html in a text editor and change the content as desired.

After making changes, rebuild the Docker image:

bash
Copy code
docker build -t my-nginx .
Restart the container to see your changes:

bash
Copy code
docker stop my-nginx-container
docker rm my-nginx-container
docker run --name my-nginx-container -d -p 8080:80 my-nginx
Troubleshooting
Port Conflicts: If you see an error about port 8080 being in use, check if another service is using that port. You can change the host port:

bash
Copy code
docker run --name my-nginx-container -d -p 8081:80 my-nginx
Repository Not Found: If you encounter "Repository not found" when pushing to GitHub, ensure that the remote URL is correct and that you have access rights.

Contributing
Contributions are welcome! If you'd like to contribute to this project, please fork the repository and create a pull request. Make sure to follow the code style and add appropriate documentation.
