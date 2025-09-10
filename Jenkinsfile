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
                script {
                    def mvnCommand = fileExists('mvnw.cmd') ? 'mvnw.cmd' : 'mvn'
                    bat "${mvnCommand} clean package"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    def mvnCommand = fileExists('mvnw.cmd') ? 'mvnw.cmd' : 'mvn'
                    bat "${mvnCommand} test"
                }
            }
        }
    }
}
