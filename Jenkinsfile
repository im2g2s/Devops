pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Replace with your GitHub repo URL
                git url: 'https://github.com/im2g2s/Devops.git', branch: 'Testing'
            }
        }

        stage('Build') {
            steps {
                echo 'Running build...'
                // Example: Python build step
                sh 'python --version'
                // Add your actual build commands here
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Example: Run pytest
                sh 'pytest tests/'
            }
        }

        stage('Report') {
            steps {
                echo 'Generating reports...'
                // Example: Allure or other reporting tools
                // sh 'allure generate ...'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
        }
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
