pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Spring Boot project...'
                sh 'mvn clean package'
            }
        }

        stage('Verify') {
            steps {
                echo 'Verifying artifact...'
                sh 'ls target'
            }
        }
    }
}
