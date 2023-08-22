# 3.11continuous-deployment-Container
Step 1: Create a New Node.js Application using Express
Install Express Generator globally (if not already installed):
![image](https://github.com/SimonLiou/3.11continuous-deployment-Container/assets/127756736/fa91a7fd-d46d-470b-9f2a-2811cc8fdcea)

2: Generate a new Express application:

![image](https://github.com/SimonLiou/3.11continuous-deployment-Container/assets/127756736/8f5b0fb1-7025-4c4e-9883-e1c1468ec40c)

Step 2: Set Up Automatic Testing using Jest
Install Jest and related dependencies:
![image](https://github.com/SimonLiou/3.11continuous-deployment-Container/assets/127756736/8a7f5d4f-4d5f-43d4-a730-ec1127b77a9e)

Create a tests/ directory in your project's root.

Write test cases in the tests/ directory using the .test.js or .spec.js file naming convention.

Update the package.json to include a test script:

![image](https://github.com/SimonLiou/3.11continuous-deployment-Container/assets/127756736/214d68e3-7144-47b7-aa12-00c06d4cf885)

Step 3: Create a Code Repository
Create a new repository on a version control platform like GitHub.

Initialize your local Git repository and connect it to the remote repository:
![image](https://github.com/SimonLiou/3.11continuous-deployment-Container/assets/127756736/788f4d64-4a09-4955-847b-fe59d67f27be)

Step 4: Create a Dockerfile
Create a Dockerfile in the project's root directory (see the example Dockerfile in the previous response).
Step 5: Set Up CI/CD Pipeline using GitHub Actions
Create a .github/workflows directory in your repository.

Create a YAML file (e.g., ci-cd.yml) in .github/workflows to define your GitHub Actions workflow (see the example YAML in the previous response).

Step 6: Push Docker Image to a Container Registry
Depending on the registry you choose (e.g., Docker Hub or AWS ECR), follow their documentation to set up authentication and obtain necessary credentials.

Add the necessary environment variables or secrets to your GitHub repository's settings to securely store registry credentials.

Step 7: Set Up Amazon ECS
In the AWS Management Console, navigate to Amazon ECS and create a new cluster.
Step 8: Configure Task Definition and Service
Create a task definition in ECS, specifying the Docker image, resources, networking, and other settings.

Create an ECS service using the task definition, specifying desired instances, scaling settings, and load balancer configurations if needed.

Step 9: Update CI/CD Pipeline for Deployment
In the GitHub Actions workflow YAML, add a step to update the ECS service after a successful build and test (see the example YAML in the previous response).
