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
                sh 'sudo aws s3  sync build/ s3://test-vk2'
            }
        }
    }
}
