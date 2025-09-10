pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/suchitra200330/springboot-ci-cd.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvnw.cmd clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvnw.cmd test'
            }
        }
    }
}

