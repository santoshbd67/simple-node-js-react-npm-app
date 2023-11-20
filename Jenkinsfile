pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh '/root/.nvm/versions/node/v14.17.6/bin/npm install'
            }
        }
        stage('Test') {
            steps {
                sh './jenkins/scripts/test.sh'
                sh 'aws s3 cp -r buil s3://test12345vk'
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}
