CI/CD Pipeline Using GitHub Actions

This project is a simple Node.js web app with a fully automated CI/CD pipeline set up using GitHub Actions.
Here’s what happens: whenever I push any changes to the main branch of this repository, GitHub automatically:
Installs all the dependencies my app needs (like Express for handling web requests).
Runs tests to make sure nothing is broken before deploying.
Builds a Docker image of the app so it can run anywhere, on any computer or server.
Pushes the image to DockerHub, so it’s ready for deployment.

All of this happens automatically, without me having to manually run commands. My DockerHub login is stored securely in GitHub as secrets, so it’s safe and never exposed in the code.
This setup makes development and deployment fast, reliable, and consistent. Anyone can now pull the Docker image and run the app with just two commands:

docker pull YOUR_DOCKER_USERNAME/nodejs-demo-app:latest
docker run -p 3000:3000 YOUR_DOCKER_USERNAME/nodejs-demo-app:latest

When the app runs, visiting http://localhost:3000 in a browser shows a simple message, confirming everything works.

In short, this project shows how to automate building, testing, and deploying a Node.js app entirely online using GitHub Actions and Docker. It’s a hands-on example of modern DevOps practices made simple.
