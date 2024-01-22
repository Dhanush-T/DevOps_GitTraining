pipeline{
    agent any
    tools {
        maven
        jdk
    }
    stages {
        stage('Build') {
            steps {
                sh "mvn clean install"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test"
            }
        }
    }
}
