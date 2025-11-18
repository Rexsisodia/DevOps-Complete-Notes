# WEEK 4 – JENKINS (CI/CD)

## 1. What is Jenkins?
- Open-source automation server for CI/CD.

## 2. Architecture
- Controller (master) + agents (workers).

## 3. Job Types
- Freestyle jobs
- Pipeline jobs

## 4. Pipeline example (Jenkinsfile)

pipeline {
  agent any
  stages {
    stage('Checkout') { steps { git 'https://github.com/user/repo.git' } }
    stage('Build')    { steps { sh 'mvn clean package' } }
    stage('Test')     { steps { sh 'mvn test' } }
    stage('Deploy')   { steps { sh './deploy.sh' } }
  }
}
