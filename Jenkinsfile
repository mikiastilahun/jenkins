pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'this is test for pull request test'
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
                s3Upload ( bucket: "desta-test", text: "if this works i need to find the artifacts")
            }
        }
    }
}