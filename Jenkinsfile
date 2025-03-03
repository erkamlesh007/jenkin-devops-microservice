pipeline {
    agent any
    environment{
        dockerHome= tool 'myDocker'
        mavenHome= tool 'myMaven'
        PATH="$dockerHome/bin:$mavenHome/bin:$PATH"
    }
    stages {
        stage('Checkout') {
            steps {
                sh 'mvn --version'
                sh 'docker --version'
                echo "Build"
                echo "PATH - $env.PATH"
                echo "BUILD_NUMBER - $env.BUILD_NUMBER"
                echo "BUILD_ID - $env.BUILD_ID"
                echo "JOB_NAME - $env.JOB_NAME"
                echo "BUILD_TAG - $env.BUILD_TAG"
                echo "BUILD_URL - $env.BUILD_URL"
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean compile'

            }
          }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Integration Test') {
            steps {
               // sh 'failsafe:integration-test failsafe:varify'
            }
        }
    }
}
