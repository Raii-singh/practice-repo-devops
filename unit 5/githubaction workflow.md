# GitHub Actions - Practice Questions & Workflow Exercises

## Q1. Identify the Error

Common YAML mistakes:

* Missing `:` after `on`
* Missing `:` after `runs-on`
* Missing `:` after `name`
* Missing `:` after `uses`

Correct workflow:

* Trigger on push
* Run build job on ubuntu
* Checkout repository code

---

## Q2. Trigger on Develop Branch

Workflow runs only when code is pushed to the `develop` branch.

---

## Q3. Hello World Workflow

Steps:

1. Checkout code
2. Print "Hello World"

Simple workflow to understand jobs and steps.

---

## Q4. Full CI Workflow

Flow:
Checkout Code → Build Project → Run Tests

Used for basic CI pipeline setup.

---

## Q5. Install Dependencies & Test

Steps:

* Install packages using `npm install`
* Run tests using `npm test`

Useful for Node.js projects.

---

## Q6. What Does This Do?

Command:
`ls`

Purpose:

* Lists files and folders in current directory.
* If checkout step is missing, repository files won't be available.

---

## Practice Scenarios

### Scenario 1

Run Ubuntu container with:

* Environment variable
* Volume mapping
* Interactive terminal

Create and edit files inside container.

### Scenario 2

Deploy MongoDB container using:

* Docker image pull
* Port mapping
* Detached mode

### Scenario 3

Run Nginx container with:

* Environment variable
* Port mapping
* Interactive mode

---

## GitHub Actions Cheatsheet

Main Components:

* Workflow
* Events
* Jobs
* Steps
* Actions
* Runners

Common Triggers:

* push
* pull_request
* schedule
* workflow_dispatch

Useful Features:

* Environment Variables
* Job Dependencies (`needs`)
* Matrix Builds
* Parallel Execution

Workflow Flow:

Trigger → Job → Steps → Action → Result
