 # Jenkins: Pipelines & CI/CD Workflows

## What is a Jenkins Pipeline?

A Jenkins Pipeline is a series of automated steps used to build, test, and deploy applications.

It follows the concept of **Pipeline as Code**, where the workflow is stored inside the project repository.

---

## Why Use Pipelines?

* Automates CI/CD process
* Reduces manual work
* Workflows are version controlled
* Easy to maintain and reuse
* Supports complex build processes

---

## Types of Pipelines

### Declarative Pipeline

* Easy to read and write
* Structured format
* Best for beginners

### Scripted Pipeline

* Uses Groovy scripting
* More flexible
* Suitable for advanced workflows

---

## Basic Pipeline Flow

Code Commit
↓
Build
↓
Test
↓
Docker Build
↓
Deploy

---

## End-to-End CI/CD Pipeline

Tools Used:

* GitHub
* Jenkins
* Maven
* Docker

Project Files:

* Application.java
* pom.xml
* Dockerfile
* Jenkinsfile

---

## Jenkinsfile

Contains all pipeline stages such as:

* Build
* Test
* Package
* Docker Build
* Deployment

Jenkins reads this file and executes the workflow automatically.

---

## Configure Pipeline in Jenkins

1. Create a new Pipeline Project
2. Open Configure
3. Select **Pipeline script from SCM**
4. Choose **Git**
5. Enter repository URL
6. Select branch
7. Set script path as `Jenkinsfile`
8. Save and Build

---

## GitHub Integration

Push project files to GitHub:

* Jenkinsfile
* Dockerfile
* pom.xml
* Source Code

Jenkins pulls code directly from GitHub and executes the pipeline.

---

## Jenkins vs GitHub Actions

### Jenkins

* Self-hosted
* Large plugin ecosystem
* Highly customizable
* Best for enterprise projects

### GitHub Actions

* Built into GitHub
* Easy setup
* Uses YAML workflows
* Good for GitHub-based projects

---

## Key Learning

* Learned Pipeline as Code concept
* Understood Declarative and Scripted Pipelines
* Connected Jenkins with GitHub repository
* Executed build process using Jenkinsfile
* Built a basic CI/CD workflow using Jenkins, Maven, and Docker
