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
                sh 'npm test'
                sh 'npm run build'
            }
        }
    }
}
