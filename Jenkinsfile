pipeline {
    agent any
    stages {
        stage('Clone sources') {
            steps {
                git branch: 'master', credentialsId: 'github', url: 'https://github.com/aphiratnimanussonkul/cd-training1.git'
            }
        }
        stage('confirm version') {
            steps {
                nodejs('node 17.9.0') {
                    sh 'node -v'
                    sh 'npm -v'
                }
            }
        }
        stage('install node packages') {
            steps {
                nodejs('node 17.9.0') {
                    sh 'npm install'
                }
            }
        }
    }
}