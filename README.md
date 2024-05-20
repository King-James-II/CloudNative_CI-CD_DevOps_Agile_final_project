# CI/CD Tax Calculator Application

The Tax Calculator is a web application designed to perform tax calculations. This README provides an overview of the project structure and the Tekton pipelines used for packaging and deployment.

## Project Structure

- `run.yaml`: Defines Tekton tasks for cleaning up workspaces, running npm install, and executing Jasmine tests.
- `pipeline.yaml`: Defines a Tekton pipeline for building and deploying the application using IBM Cloud Code Engine.
- `tasks.yaml`: Defines Tekton tasks for cleaning up workspaces, running npm install, and executing Jasmine tests.

## Tekton Pipelines

### Cleanup Task

This task cleans up the workspace by deleting all files.

### NPM Task

This task installs npm dependencies for the application.

### Jasmine Task

This task runs Jasmine tests for the application.

### Pipeline

The pipeline orchestrates the tasks in the following sequence:
1. Cleanup
2. Clone repository
3. NPM install
4. Jasmine tests
5. Build Docker image

## User Stories

User stories have been created and added to the project's ZenHub board for:
- Containerizing the Application
- Deploying on IBM Cloud
- Creating Pipeline for Packaging and Deploying the Application
