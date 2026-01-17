# Node.js Todo List App

### 🎯 Project Overview
A simple, containerized ToDo application built with **Node.js**, showcasing a complete DevOps workflow with Dockerized deployment and an automated CI/CD pipeline using **Jenkins**.

**Tech Stack**
1. **Backend:** Node.js, Express, EJS
2. **Testing:** Mocha, Chai, Supertest
3. **DevOps:** Docker, Jenkins, Git

### ⚙️ Architect Diagram
![Architect Diagram](./assets/workflow.png)


### 📋 Prerequisites

Before you start, make sure you have installed:

| Tool        | Purpose                                                     | Documentation |
|-------------|-------------------------------------------------------------|---------------|
| **Node.js** | The runtime environment used to build and run the application | [Install Node.js](https://nodejs.org/en/download)           |
| **Docker**  | Builds and runs container images for application services | [Install Docker](https://docs.docker.com/engine/install/)       |
| **Jenkins** | The automation server that handles the CI/CD pipeline     | [Install Jenkins](https://www.jenkins.io/doc/book/installing/)  |


### 💻 How to Run Locally

```sh
# Install Dependencies
npm install

# Run the Application
npm start

# Access the app in your browser http://localhost:8000/todo
```
![ToDo](./assets/verify.png)


### 🔄 Jenkins CI/CD Pipeline
The **Jenkinsfile orchestrates the entire build and run process**, from dependency installation to Docker image creation and automated deployment.

**I. Pipeline Stages:**
1. **Checkout:** Pulls code from GitHub.
2. **Install Dependencies:** Runs `npm ci` for a clean install.
3. **Build Image:** Creates a Docker image with the build number tag.
4. **Push to Docker Hub:** Pushes the image to docker hub with image tag.
5. **Deploy:** Stops the old container and runs the new one automatically.
6. **Health Check:** Verifies that the app is responding correctly.

**II. Jenkins Requirements:**
1. **Plugins:** Docker Pipeline, NodeJS, Git.
2. **Credentials:** (Token) for Docker Hub access.
3. **Tools:** NodeJS configured in Global Tool Configuration.


### 🚀 Features
1. **CRUD Operations**: Add, Edit, and Delete todo items.
2. **Clean UI**: Server-side rendering using EJS templates.
3. **Automated Testing**: Unit tests using Mocha, Chai, and Supertest
4. **Dockerized**: specific `Dockerfile` for production-ready container image.
5. **CI/CD Ready**: Complete `Jenkinsfile` for automated build and deployment.
