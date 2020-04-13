pipeline {
    agent any
    tools {
        maven 'maven363' 
    }
    stages {
        stage ('Unit test') {
            steps {
                sh 'mvn test'
            }    
        }   
        
         stage('Package') {
             steps {
                sh 'mvn package -DskipTest'
            }
         }  
        stage('Build and Run docker image') {
             steps {
                sh 'docker build -t freemanpolys/test:v1.0.0 .'
                sh 'docker rm -f test'
                sh 'docker run --name test -d -p 8088:8088 freemanpolys/test:v1.0.0'
            }
         }         

    }

    post {
        always {
            junit 'target/surefire-reports/**/*.xml'
            archiveArtifacts artifacts: 'target/*.jar'
        }
    }
}
