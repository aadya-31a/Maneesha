pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Code checked out from GitHub'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                bat 'javac App.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running application...'
                bat 'java App'
            }
        }
    }

    post {
        success {
            echo 'Build SUCCESS'
        }
        failure {
            echo 'Build FAILED'
        }
    }
}
