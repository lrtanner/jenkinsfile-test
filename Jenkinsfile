pipeline {
    agent none
    stages {
        stage('Build') {
            agent { label "nodejs" }
            steps {
                echo 'Building..'
                sh 'ls'
                sh (
                        script: './echo.sh',
                        returnStatus: true
                )
//                echo bat (
//                        script: 'dir',
//                        returnError: true
//                )
            }
        }
        stage('Test') {
            agent any
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            agent any
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            agent any
            archiveArtifacts artifacts: '**/*.jar', fingerprint: true
        }
    }
}