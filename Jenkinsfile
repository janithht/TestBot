pipeline {
    agent {
        node {
            label 'docker-agent'
        }
    }
    triggers {
        pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'javac Hello.java'
                sh 'java Hello'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '''
                    echo "Running unit tests..."
                '''
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh '''
                    echo "Deploying to production..."
                '''
            }
        }
    }
}
