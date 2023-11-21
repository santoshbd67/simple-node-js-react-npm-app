pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'id'
                sh 'sudo $(nvm which npm) install'
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
