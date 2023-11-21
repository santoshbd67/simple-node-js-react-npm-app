pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'sudo /root/.nvm/versions/node/v14.17.5/bin/npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
                sh 'npm run build'
            }
        }
    }
}
