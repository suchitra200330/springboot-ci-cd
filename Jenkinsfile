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
                    // Check if mvnw.cmd exists, otherwise fall back to system-installed Maven
                    def mvnCommand = fileExists('mvnw.cmd') ? 'mvnw.cmd' : 'mvn'
                    bat "${mvnCommand} clean package"
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Check if mvnw.cmd exists, otherwise fall back to system-installed Maven
                    def mvnCommand = fileExists('mvnw.cmd') ? 'mvnw.cmd' : 'mvn'
                    bat "${mvnCommand} test"
                }
            }
        }
    }
}
