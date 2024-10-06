pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the latest code from Bitbucket
                git branch: 'main', url: 'git@github.com:bharatgadhe/java.git', credentialsId: '7cbbe4fb-3a87-4b05-b54c-bd48c5594898'
            }
        }
        
        stage('Build') {
            steps {
                // Add build steps here
                echo 'Building the project...'
                // e.g., sh './build.sh' or similar commands
            }
        }

        stage('Test') {
            steps {
                // Add test steps here
                echo 'Running tests...'
                // e.g., sh './run-tests.sh' or similar commands
            }
        }

        stage('Deploy') {
            steps {
                // Add deploy steps here
                echo 'Deploying application...'
                // e.g., sh './deploy.sh' or similar commands
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed.'
        }
    }
}
