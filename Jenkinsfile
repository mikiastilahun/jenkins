pipeline {
    agent { docker { image 'index.docker.io/mikeabebe/node-test:v1' } }
    stages {
        stage('build') {
            steps {
                sh 'echo "jenkins is working fine"'
            }
        }
    }
}