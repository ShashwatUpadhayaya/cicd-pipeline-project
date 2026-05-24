pipeline {
    agent any
    stages{
        stage('checkout') {
            steps{
                echo 'Pulling latest code from GitHub'
                checkout scm
            }
        }
        stage('Test code') {
            steps{
                echo 'Checking the syntax'
                bat 'python -m py_compile main.py'
            }
        }
        stage('Build docker image'){
            steps{
                echo 'Building docker image'
                bat 'docker build -t my-fastapi-app-automated'
            }
        }
    }
}