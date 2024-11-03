# Flask Web App with Jenkins and Docker

This repository contains a basic Flask web app, a Dockerfile to containerize it, and a Jenkins pipeline to automate building and deployment.

## Files in This Repo
- **`app.py`**: A minimal Flask app that returns "Hello, Jenkins!" on the home page.
- **`Dockerfile`**: Docker configuration to build the app image.
- **`Jenkinsfile`**: Jenkins pipeline with two stages:
  - **Build**: Builds a Docker image from the Dockerfile.
  - **Deploy**: Runs a container from the image, exposing it on port 5000.

## Prerequisites
- **Docker**: Install Docker Desktop for Windows to build and run containers.
- **Jenkins**: Set up Jenkins with Docker access.

## Quick Start
To get started, follow these steps:

```bash
:: 1. Clone the Repo
git clone <repository_url>
cd <repository_name>

:: 2. Run the App Locally (Optional)
docker build -t myflaskapp .
docker run -p 5000:5000 myflaskapp
:: Visit http://localhost:5000 to see "Hello, Jenkins!"

:: 3. Set Up the Jenkins Pipeline
:: In Jenkins:
:: - Create a new Pipeline job.
:: - Choose "Pipeline script from SCM" and enter your repo URL.
:: - Jenkins will use the Jenkinsfile automatically.
:: - Run the pipeline to build and deploy the app.

:: 4. Access the App
:: After deployment, go to http://localhost:5000 to see "Hello, Jenkins!"
