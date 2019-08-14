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
                s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: true,includePathPattern: "*" ,verbose: true, entries: [[bucket: 'dober', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: false, noUploadOnFailure: false, showDirectlyInBrowser: false,  storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'desta-test', userMetadata: []
            }
        }
    }
}