pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git credentialsId: 'github-credentials', branch: 'main', url: 'https://github.com/hearty101224/jenkins-ci-cd-demos.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
            }
        }

        stage('Test') {
            steps {
                bat 'python -m unittest discover'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application..."
            }
        }
    }
}
