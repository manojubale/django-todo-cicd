pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checkout completed'
            }
        }

        stage('Debug') {
            steps {
                sh '''
                echo "Current Directory:"
                pwd

                echo "Workspace:"
                ls -la

                echo "Dockerfile:"
                find . -name Dockerfile
                '''
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t django-todo .'
            }
        }

        stage('Run') {
            steps {
                sh 'docker run -d -p 8000:8000 --name Django-todo django-todo'
            }
        }
    }
}
