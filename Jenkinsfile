pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo "Pulling code from repository"
                checkout scm
            }
        }

        // stage('Setup Python') {
        //     steps {
        //         echo "Setting up Python environment"
        //         sh 'python3 --version'
        //     }
        // }

        stage('Run Python Script') {
            steps {
                echo "Executing Python script"
                sh 'python3 app.py'
            }
        }
    }

    post {
        success {
            echo "Pipeline executed successfully!"
        }
        failure {
            echo "Pipeline failed!"
        }
    }
}
