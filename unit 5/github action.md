# GitHub Actions: Core Concepts

## What is GitHub Actions?

GitHub Actions is a CI/CD (Continuous Integration and Continuous Deployment) tool provided by GitHub. It helps automate tasks such as building, testing, and deploying applications directly from a GitHub repository.

---

## Core Concept

### 1. Workflow

A workflow is an automated process defined inside a YAML file. It contains one or more jobs and runs when a specific event occurs.

Example:

* Push to repository
* Pull request creation
* Manual trigger

---

### 2. Events

Events are actions that trigger workflows.

Common events:

* push
* pull_request
* workflow_dispatch
* release

---

### 3. Jobs

A job is a set of steps that execute on the same runner.

Example:

* Build application
* Run tests
* Deploy application

Multiple jobs can run in parallel or sequentially.

---

### 4. Steps

Steps are individual tasks inside a job.

Examples:

* Checkout code
* Install dependencies
* Run tests
* Build project

---

### 5. Actions

Actions are reusable units of code that perform specific tasks.

Example:

* actions/checkout
* actions/setup-node

They help reduce repeated code in workflows.

---

### 6. Runners

A runner is the machine that executes workflow jobs.

Types:

* GitHub-hosted runners
* Self-hosted runners

GitHub-hosted runners come with common tools pre-installed.

---

## Workflow Structure

Workflow → Jobs → Steps → Actions

---

## Benefits of GitHub Actions

* Automates repetitive tasks
* Improves development workflow
* Supports CI/CD pipelines
* Easy integration with GitHub repositories
* Faster testing and deployment

---

## Conclusion

GitHub Actions helps automate software development processes. By using workflows, jobs, steps, actions, and runners, developers can build efficient CI/CD pipelines and reduce manual work.
