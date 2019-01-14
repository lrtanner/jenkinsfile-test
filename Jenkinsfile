node {
    stage('Build') {
        echo 'Checking out repo...'
        checkout scm
    }
    stage('Test') {
        echo 'Testing....'
        sh (
                script: 'ls -l',
                returnStdout: true
        )
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}