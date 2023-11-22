
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
                sh 'aws s3 cp build.zip s3://bucketss12/build'
            }
        }
    }
}
