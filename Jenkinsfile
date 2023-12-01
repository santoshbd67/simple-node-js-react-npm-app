pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('docker_login')
    }
    stages {
            stage('Build docker Image') {
                steps {
                    sh 'sudo docker build -t simple-nodejs:1.0 .'
                    tage('Docker login') {
                        steps{
                            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                            stage('push to dockerhub') {
                                steps{
                                    sh 'docker push simple-nodejs:1.0'
                                }
                            }
                        }
                    }
                }
            }
        }
    }

