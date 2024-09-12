pipeline {
    agent {
       node  {
            label 'Docker-agent'  
            }
      }
    triggers{
      pollSCM '* * * * *'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'javac hello.java'
                sh 'java hello'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                sh '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh '''
            }
        }
    }
}