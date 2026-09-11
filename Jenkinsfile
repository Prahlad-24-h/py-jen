pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'YOUR_GITHUB_REPOSITORY_URL'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Test') {
            steps {
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                sh 'python app.py'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
