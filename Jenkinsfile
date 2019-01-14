pipeline {
    agent none
    stages {
        stage('Build') {
            agent { label "nodejs" }
            steps {
                echo 'Building..'
                sh (
                    script: 'echo.sh'
                )
                echo bat (
                        script: 'dir',
                        returnStdout: true
                )
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
            archiveArtifacts artifacts: '**/*.jar', fingerprint: true
        }
    }
}