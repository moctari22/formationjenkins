pipeline {
    agent any 
    tools {
        maven 'maven385' 
    }
    stages {
        stage('Get maven version') {
            steps {
                bat 'mvn --version' 
            }
        }
    }
}
