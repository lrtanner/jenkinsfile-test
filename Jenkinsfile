pipeline {
    agent none
    stages {
        stage('Build') {
            agent { label "nodejs" }
            steps {
                echo 'Building..'
                sh 'ls'
                sh './echo.sh'
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
        agent any
        always {
            archiveArtifacts artifacts: '**/*.jar', fingerprint: true
        }
    }
}