pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'javac src\\Main.java'
            }
        }

        stage('Test') {
            steps {
                bat 'java -cp src Main'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }

        failure {
            echo 'Pipeline failed!'
        }
    }
}
