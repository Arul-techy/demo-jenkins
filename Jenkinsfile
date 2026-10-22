pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
                echo 'Source code retrieved successfully'
            }
        }

        stage('Build') {
            steps {
                bat 'if exist index.html (echo HTML file found) else (exit /b 1)'
                echo 'Build completed successfully'
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
