pipeline {
    agent any 
    tools {
        maven 'maven385' 
    }
    stages {
        parallel{
            stage('Get version') {
                steps {
                    echo 'Le step de Get version'
                    bat 'mvn --version' 

                }

            }
          stage('Unit test') {
              steps {
                    echo 'Le step de test'
                    bat 'mvn test'
                }

            }
        }
      stage('Packaging') {
        steps {
            echo 'Le step de Packaging' 
            bat 'mvn package -DskipTest'
        }

    }
    }
}

