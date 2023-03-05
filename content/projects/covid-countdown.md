---
title: "Deploying a COVID Countdown Application with Docker and AWS"
description: "This post describes the deployment of a COVID Countdown Application using Docker and AWS, highlighting the use of Jenkins to automate the deployment process."
dateString: May 2022
draft: false
tags: ["Docker", "Jenkins", "AWS", "CI/CD"]
showToc: false
weight: 205
cover:
    image: "projects/face-landmarks-detection/cover.jpeg"
--- 

# Introduction

In this post, I'll walk you through how I deployed a test application using Docker and AWS. Specifically, I created two AWS EC2 instances - one to host Jenkins and another to run the application using Docker. The application I deployed is a simple web application that displays a countdown to the end of the COVID-19 pandemic.

## The Application
The application I deployed is a simple web application that displays a countdown timer to the end of the COVID-19 pandemic. It can be found on [Docker Hub](https://hub.docker.com/u/roodrigohsoares) as a pre-built Docker image.

## The Setup
To get started, I created two EC2 instances on AWS. One instance was used to run Jenkins, and the other instance was used to run the Docker container that hosted the application.

## Jenkins Instance
I chose to use Jenkins to automate the deployment process because it's a powerful, open-source automation server that allows for easy configuration and management of software builds, tests, and deployments.

After creating the EC2 instance, I installed Jenkins using the official Jenkins documentation. Once Jenkins was installed, I created a new job that pulled the Docker image from Docker Hub, stopped and removed any previous containers, and started a new container with the latest image.

## Application Instance
On the other EC2 instance, I installed Docker and pulled the application Docker image from Docker Hub. I then started a new container with the image and exposed the necessary port to the internet.

# Conclusion
In conclusion, deploying the COVID Countdown application using Docker and AWS was a great exercise in improving my deployment skills. By using Jenkins, I was able to automate the deployment process and make it more reliable and repeatable. Additionally, using Docker allowed for easy management and scaling of the application, making it a great choice for deploying applications in a production environment.