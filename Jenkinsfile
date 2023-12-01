
pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'id'
                sh 'npm  install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
                sh 'npm run build'
                sh ' zip build.zip *'
                 }
            stage('Build docker Image'){
                steps {
                    sh 'docker build -t simple-nodejs:1 .'
                }
            }
        }
    }
}
