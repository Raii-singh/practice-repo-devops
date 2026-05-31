# GitHub Actions Workflow with Docker

## Objective

Create a Flask application, containerize it using Docker, and automate image building using GitHub Actions whenever code is pushed.

---

## Project Structure

my-docker-app/

├── app.py

├── requirements.txt

├── Dockerfile

└── .github/workflows/ci-cd.yml

---

## Steps Performed

### 1. Create Project Folder

* Create project directory
* Move into the folder

### 2. Create Flask App

* Create `app.py`
* Simple route `/`
* Returns: "Hello from Docker CI/CD!"

### 3. Add Requirements

* Create `requirements.txt`
* Add Flask dependency

### 4. Create Dockerfile

* Use `python:3.9-slim`
* Set working directory
* Copy project files
* Install dependencies
* Run application

### 5. Configure GitHub Actions

Create workflow file:

`.github/workflows/ci-cd.yml`

Workflow:

* Trigger on push to `main`
* Checkout repository
* Build Docker image
* Display available Docker images

### 6. Push Code to GitHub

* Initialize git repository
* Commit files
* Connect remote repository
* Push code to main branch

### 7. Verify Workflow

* Open repository on GitHub
* Go to Actions tab
* Check CI-CD Pipeline status
* Green tick means success

### 8. Add GitHub Secrets

For future Docker Hub integration:

* DOCKERHUB_USERNAME
* DOCKERHUB_TOKEN

---

## Run Application Locally

Build Image:

* docker build -t my-docker-app .

Run Container:

* docker run -p 5000:5000 my-docker-app

Open Browser:

* http://localhost:5000

Output:
Hello from Docker CI/CD!

---

## Workflow Flow

Push Code
↓
GitHub Actions Triggered
↓
ubuntu-latest Runner
↓
Checkout Repository
↓
Build Docker Image
↓
Verify Image using docker images
↓
Workflow Success ✅

---

## Key Learning

* Created a Flask web application
* Built a Docker image using Dockerfile
* Automated build process using GitHub Actions
* Verified workflow execution from GitHub Actions tab
* Learned basic CI/CD pipeline setup
