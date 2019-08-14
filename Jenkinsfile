pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'this is from the fork'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing.'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}