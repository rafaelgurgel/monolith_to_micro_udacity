# Udacity Monolith to Microservice Udagram Project

Convert a monolith application to microservice arquitecture

# Installation

Requirements:
  1.1 Install Docker + Docker-compose
  1.2 Install all required dependencies
  1.3 Set the needed/desired env variables in the env.model file and rename it to '.env' to run

Procedure:
  1. Go to the 'udacity-c3-deployment directory
  2. Build: `docker-compose -f docker-compose-build.yaml build --parallel`
  3. Push Images: `docker-compose -f docker-compose-build.yaml push`
  4. Start the containers with 'docker-compose up'

Kubernettes:
  1. Create Cluster with `eksctl create cluster --name udagram`
  2. Create travis user with `eksctl create iamidentitymapping --name  udagram --role arn:aws:iam::?:role/travis_eks --group system:masters --username travis_eks`
  3.Start the pipeline