pipeline {
    agent any 
    tools {
        maven 'maven385' 
    }
    stages {
        stage('Unit test') {
            steps {
                echo 'Le step de test'
                bat 'mvn --version' 
                bat 'mvn test'
            }
        }
    }
}

