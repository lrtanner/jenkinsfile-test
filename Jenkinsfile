pipeline {
    agent any

    stages {
        agent { label "nodejs" }
        stage('Build') {
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