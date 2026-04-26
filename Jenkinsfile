pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Verify Artifact') {
            steps {
                sh 'ls target'
            }
        }

        stage('Upload to Nexus') {
            steps {
                sh '''
                curl -v -u admin:Claudiarenee1 \
                --upload-file target/demo-0.0.1-SNAPSHOT.jar \
                http://10.17.10.121:8081/repository/homework6/com/example/demo/0.0.1-SNAPSHOT/demo-0.0.1-SNAPSHOT.jar
                '''
            }
        }
    }
}
