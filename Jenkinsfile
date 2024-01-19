pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from Git repository
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 
                sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run a simple test (replace with your actual test command)
                sh 'mvn test'
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded! Deploy or perform additional tasks here.'
        }
        failure {
            echo 'Pipeline failed! Notify or take corrective actions here.'
        }
    }
}
