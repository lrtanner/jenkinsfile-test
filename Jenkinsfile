pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                bat (
                    script: 'echo.bat'
                )
                echo bat (
                        script: 'dir',
                        returnStdout: true
                )
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