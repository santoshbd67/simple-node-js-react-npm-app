pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('docker_login')
        IMAGE_NAME = 'test-nodejs/new'
        IMAGE_TAG = '1.0'
    }
    stages {
            stage('Build docker Image') {
                steps {
                    sh 'sudo docker build -t test-nodejs:1.0 .'
                }
            }
                    stage('Docker login') {
                        steps{
                            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                        }
                    } 
                        stage('push to dockerhub') {
                                steps{
                                    sh 'sudo docker push test-nodejs:1.0'
                                }
                            }
                        }
                    }
                
            
        
    

