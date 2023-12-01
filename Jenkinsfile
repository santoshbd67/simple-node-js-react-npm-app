pipeline {
    agent any
    environment {
        DOCKERHUB_CREDENTIALS = credentials('docker_login')
    }
    stages {
            stage('Build docker Image') {
                steps {
                    sh 'sudo docker build -t simple-nodejs:1.0 .'
                }
            }
                    stage('Docker login') {
                        steps{
                            sh 'echo $DOCKERHUB_CREDENTIALS_PSW | sudo docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
                        }
                    } 
                        stage('push to dockerhub') {
                                steps{
                                    sh 'sudo docker push simple-nodejs:1.0/new'
                                }
                            }
                        }
                    }
                
            
        
    

