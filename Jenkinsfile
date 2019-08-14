pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'this is test for pull request test just some changes'
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
                sh "ls"
                s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'dober', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, showDirectlyInBrowser: false, file: 'index.html', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'desta-test', userMetadata: []
            }
        }
    }
}