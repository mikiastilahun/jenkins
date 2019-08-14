#!/bin/bash
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
                echo 'Deploying..'
                sh "ls"
                sh "/usr/bin/aws s3 sync . s3://desta-test"
                 }
        }
    }
}