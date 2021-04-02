pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -Ptest'
            }
        }
        stage('Deliver') {
            steps {
                sh 'ls -R; sleep 100'
            }
        }
    }
}
