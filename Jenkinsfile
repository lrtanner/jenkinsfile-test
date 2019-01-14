node {
    stage('Build') {
        echo 'Checking out repo...'
        checkout scm
    }
    stage('Test') {
        echo 'Testing....'
        bat (
            script: 'dir',
            returnStdout: true
        )
    }
    stage('Deploy') {
        echo 'Deploying....'
    }
}