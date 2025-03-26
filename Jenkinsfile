pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Pulling code from repository'
                checkout scm
            }
        }

        stage('Run Python Script') {
            steps {
                echo 'Executing Python script'
                bat 'python app.py'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
