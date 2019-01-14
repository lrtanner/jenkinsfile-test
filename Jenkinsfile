//node {
//    stage('Build') {
//        echo 'Building....'
//    }
//    stage('Test') {
//        echo 'Testing....'
//        echo bat (
//            script: 'dir',
//            returnStdout: true
//        )
//    }
//    stage('Deploy') {
//        echo 'Deploying....'
//    }
//}

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
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
}