pipeline{
    agent any
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
    post {
        always {
            junit (
                allowEmptyResults: true,
                testResults: "*/test-reports/.xml"
            )
        }
    }
}
