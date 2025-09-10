pipeline {
    agent any

    tools {
        maven 'Maven'     // the Maven installation name you added in Jenkins
        git 'Default'     // optional, if you defined Git in Jenkins tools
    }

    stages {
        stage('Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/suchitra200330/springboot-ci-cd.git'
            }
        }

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                bat 'mvn test'
            }
        }
    }
}
