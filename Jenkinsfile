pipeline {
    agent any
    stages {
        stage('maven package') {
            steps {
                withMaven(jdk: 'jkd 8', maven: 'maven-3', publisherStrategy: 'EXPLICIT') {
    // some bloc
                sh "mvn clean"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
    }
}
