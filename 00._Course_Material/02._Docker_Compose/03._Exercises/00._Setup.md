# Setup

Throughout these exercises, we will be using the same Spring Boot application, where the endgoal is to dockerize the application as well as the database, using Docker Compose.

To achieve this, you will need to fork and clone a GitHub repository containing the Spring Boot application code.

## Goal
Use one Spring Boot application across all exercises, ending with a Docker Compose stack for app + database.

## Step 1: Fork the repository

Fork [this repository](https://github.com/ek-osnb/docker-spring) i.e. creating a copy of the original repository under your own GitHub account.

Then clone the forked repository to your local machine (using the SSH URL)
```bash
git clone <repo-name>
```

## Step 2: Open the project in IntelliJ

Open IntelliJ IDEA, and import the project to your workspace.

## Step 3: Run the application

Check if the application runs.

The application has only one endpoint: `GET /api/messages`
