pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    docker.image('maven:3.6.3').inside {
                        sh 'mvn --version'
                    }
                }
            }
        }
    }
}
