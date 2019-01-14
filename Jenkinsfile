node {
    stage('Build') {
        echo 'Building....'
    }
    stage('Test') {
        echo 'Testing....'
        echo bat (
            script: 'dir',
            returnStdout: true
        )
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}