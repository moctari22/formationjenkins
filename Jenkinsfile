pipeline {
    agent any 
    tools {
        maven 'maven385' 
    }
    stages {
        stage('Unit test') {
            steps {
                sh 'mvn test' 
            }
        }
        stage('Package') {
            steps {
                sh 'mvn package -DskipTest' 
            }
        }
    }
}
