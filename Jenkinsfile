pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    credentialsId: 'github-token',
                    url: 'https://github.com/hearty101224/jenkins-ci-cd-demos.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                bat 'python app.py'  // This will print the output of app.py
            }
        }

        stage('Test') {
            steps {
                bat 'python -m unittest discover || echo "Tests failed, but continuing..."'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
}
