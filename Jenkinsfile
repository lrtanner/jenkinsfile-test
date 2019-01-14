pipeline {
    agent any
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
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '**/*.jar', fingerprint: true
        }
    }
}