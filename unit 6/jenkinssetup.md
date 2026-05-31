# Jenkins: Setup, Installation & Plugins

## Jenkins Installation

### Installation Methods

**Docker (Recommended)**

* Run Jenkins container using Docker
* Easy setup and practice

**JAR File**

* Run using `java -jar jenkins.war`

**System Install**

* Download installer from Jenkins website
* Install like a normal application

---

## First Access

* Open: `http://localhost:8080`
* Enter admin password
* Install suggested plugins
* Create admin user
* Login to Jenkins dashboard

---

## Creating First Job

Steps:

1. Click **New Item**
2. Enter job name
3. Select **Freestyle Project**
4. Configure Git repository
5. Add build trigger
6. Add build steps
7. Save and click **Build Now**

A Job is simply a set of instructions telling Jenkins what to do and when to do it.

---

## Jenkins Plugins

Plugins extend Jenkins functionality and integrate it with other tools.

Without plugins, Jenkins provides only basic automation features.

---

## Important Plugins

* Git Plugin → Connect Git repositories
* Maven Integration → Build Java projects
* Docker Plugin → Work with containers
* Docker Pipeline → Use Docker in pipelines
* Pipeline Plugin → CI/CD as code
* HTML Publisher → Publish reports
* SSH Agent → Remote deployment
* Role-based Authorization → Access control
* Slack Notification → Build alerts

---

## Installing Plugins

1. Open Jenkins Dashboard
2. Go to **Manage Jenkins**
3. Click **Manage Plugins**
4. Search required plugin
5. Install and restart if needed

Note:
Installing too many plugins can affect performance and may create compatibility issues.

---

## Common Plugins for CI/CD

* Pipeline Graph Analysis
* Pipeline REST API
* Pipeline Stage View
* Maven Integration
* Docker Commons
* Docker Pipeline
* Git Server
* SSH Agent
* HTML Publisher
* Role-based Authorization Strategy

---

## Key Learning

* Installed Jenkins using different methods
* Accessed Jenkins dashboard
* Created first Freestyle Job
* Understood the role of plugins
* Learned commonly used CI/CD plugins
    