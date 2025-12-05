STAA-Automating-CICD-Pipeline-SpringBoot-AWS/
│
├── README.md
├── .gitignore
├── pom.xml
├── Dockerfile
├── buildspec.yml
├── ecs-task-definition.json
│
├── src/
│   └── main/java/com/staa/app/Application.java
│   └── main/java/com/staa/app/controller/HelloController.java
│   └── resources/application.properties
│
├── .mvn/wrapper/*
├── mvnw
├── mvnw.cmd
│
├── pipeline/
│   ├── codebuild-project.json
│   ├── codepipeline.json
│   ├── iam-roles.json
│
└── infrastructure/
    └── ecs-cluster-cfn.json (optional)
DevOps on AWS: Automating CI/CD Pipeline for Spring Boot Application Deployment
DevOps on AWS Banner 
Course-End Project
This repository contains the implementation for the course-end project focused on automating a CI/CD pipeline using AWS services to deploy a Spring Boot application on Amazon ECS with Docker. It integrates AWS CodePipeline, CodeBuild, and ECR for seamless updates and deployments.

Objective
To implement a CI/CD pipeline using AWS services for automating the deployment of a Spring Boot application on Amazon ECS with Docker, integrating CodePipeline, CodeBuild, and ECR for seamless updates.

Problem Statement and Motivation
Real-time Scenario
Imagine a retail company that has a Spring Boot-based inventory management system. The system is used by several departments and is hosted in containers to ensure scalability.
The company wants to reduce the manual intervention required to deploy updates by automating the build and deployment process. By setting up a CI/CD pipeline, developers can push updates to a GitHub repository, automatically triggering a sequence of actions that build, containerize, and deploy the application without downtime. This ensures faster and more reliable system updates, minimizing operational delays.

Industry Relevance
The following are the DevOps tools and AWS services used in this project:

AWS CodePipeline: A CI/CD service that automates the build, test, and deployment process of the application through a defined pipeline.
AWS CodeBuild: A fully managed build service that compiles source code, runs tests, and produces software packages ready for deployment.
AWS ECR (Elastic Container Registry): A fully managed Docker container registry that stores, manages, and deploys Docker container images.
AWS ECS (Elastic Container Service): A scalable container orchestration service that enables you to run, stop, and manage containers on a cluster.
Docker: A platform for developing, shipping, and running applications inside lightweight, portable containers.
IAM (Identity and Access Management): AWS service used to manage access to AWS resources, providing necessary permissions for CodeBuild and ECS.
GitHub: A source code hosting platform that stores the Spring Boot application repository and integrates with the CI/CD pipeline.


Tasks
The following tasks outline the CI/CD pipeline creation process:

Fork the Spring Boot project GitHub repository and create an ECR to store the Docker images.
Modify the build configuration file in the GitHub repository to include the ECR image URI.
Create a CodeBuild project to pull code from the GitHub repository.
Create an ECS cluster using the Fargate launch type and configure an ECS service to run tasks on the cluster.
Deploy the application.
Configure CodePipeline to trigger on GitHub changes, integrating CodeBuild and ECS for automated deployment.
Test and monitor the pipeline execution in AWS CodePipeline.
