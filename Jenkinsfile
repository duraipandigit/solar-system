pipeline {
    agent any

    tools {
        nodejs 'NodeJS247'   
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/duraipandigit/solar-system.git', branch: 'main', credentialsId: 'GitHub_Token'
            }
        } 
        stage('Check Node Version') {
            steps {
                sh 'node -v'
                sh 'npm -v'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
    }
}
