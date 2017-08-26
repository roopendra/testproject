pipeline {
    agent any 

    stages {
        stage('Build') { 
            steps { 
                'mvn clean build'
            }
        }
        stage('Test'){
            steps {
                'mvn test'
            }
        }

    }
}
