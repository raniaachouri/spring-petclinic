pipeline {
    agent any

    tools {
        maven 'Maven-3.6.3'   // ou le nom configuré dans Jenkins
        jdk 'JDK17'           // ou ton JDK configuré
    }

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/<ton-user>/spring-petclinic.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
