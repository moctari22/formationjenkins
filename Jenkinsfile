pipeline {
    agent any 
    tools {
        maven 'maven385' 
    }
    stages {
        stage('Get maven version') {
            steps {
                sh 'mvn --version' 
            }
        }
    }
}
