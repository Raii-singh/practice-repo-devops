# CI Pipeline: Build & Push Docker Image to Docker Hub

## Objective

Create a GitHub Actions CI pipeline that:

* Triggers on every push to `main`
* Builds Docker image
* Logs in to Docker Hub
* Pushes image to Docker Hub automatically

---

## Pre-requisites

### Docker Hub Access Token

* Login to Docker Hub
* Go to Security → Create Access Token
* Copy and save the token

### GitHub Secrets

Add these secrets in:
Settings → Secrets and Variables → Actions

* DOCKERHUB_USERNAME
* DOCKERHUB_TOKEN

Secrets keep sensitive information secure and hidden from logs.

---

## Project Files

* app.py
* requirements.txt
* Dockerfile
* .github/workflows/docker-ci.yml

---

## Workflow Steps

### 1. Trigger Workflow

Runs automatically when code is pushed to `main`.

### 2. Checkout Repository

Downloads repository code to the GitHub runner.

### 3. Login to Docker Hub

Uses GitHub Secrets for authentication.

### 4. Build Docker Image

Creates Docker image from Dockerfile.

Image Tag:
`username/app-ci:latest`

### 5. Push Image

Uploads image to Docker Hub repository.

---

## Workflow Flow

Push Code
↓
GitHub Actions Triggered
↓
Checkout Repository
↓
Docker Hub Login
↓
Build Docker Image
↓
Push Image to Docker Hub
↓
Workflow Success ✅

---

## Environment Variables

Environment variables are key-value pairs used for configuration.

Example:

* APP_NAME
* APP_PORT

Used for:

* Application settings
* Ports
* Environment names

---

## Secrets

Secrets are encrypted values stored in GitHub.

Used for:

* Passwords
* Tokens
* API Keys

Example:

* DOCKERHUB_USERNAME
* DOCKERHUB_TOKEN

Secrets are hidden in logs and provide better security.

---

## Environment Variables vs Secrets

Environment Variables:

* Used for normal configuration
* Visible during execution

Secrets:

* Used for sensitive information
* Encrypted and hidden

---

## Verification

After successful workflow execution:

* Open Docker Hub
* Check repository `username/app-ci`
* Verify latest image is available

---

## Testing Published Image

Pull Image:
`docker pull yourusername/app-ci:latest`

Run Container:
`docker run -p 5000:5000 yourusername/app-ci:latest`

Open:
`http://localhost:5000`

Output:
Hello from Docker CI/CD!

---

## Key Learning

* Automated Docker image build process
* Integrated GitHub Actions with Docker Hub
* Used GitHub Secrets for secure authentication
* Learned difference between Environment Variables and Secrets
* Implemented a basic CI pipeline
