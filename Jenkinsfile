pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('id')
    }
    stages {
            stage('Build docker Image') {
                steps {
                    sh 'sudo docker build -t simple-nodejs:1.0 .'  
                }
            }
        }
    }

