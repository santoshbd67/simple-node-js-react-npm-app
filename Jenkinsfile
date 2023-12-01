
pipeline {
    agent any
    stages {
            stage('Build docker Image') {
                steps {
                    sh 'sudo docker build -t simple-nodejs:1.0 .'
                    stage('Login dockerhub') {
                        steps {
                            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                            {
                                {
                                   stage('Push') {
                                       steps {
                                           sh 'docker push simple-nodejs:1.0 '
                                       }
                                   }
                }
            }
        }
    }

