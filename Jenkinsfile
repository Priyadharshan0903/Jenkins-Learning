pipeline {
    agent any

    tools {
        nodejs 'NoeJS 26.7.0'
    }
    stages {
        stage('checkout') {
         steps {
            checkout scm
         }
        }

        stage('install') {
            steps {
                sh 'npm install'
            }
        }
    }
    post {
        success {
            echo "Build Succeeded"
        }
        failure {
            echo "Build failed"
        }
    }
}
