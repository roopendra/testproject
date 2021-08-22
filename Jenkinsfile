pipeline {
   agent any    
    
    stages {
        stage('Build') {
            steps {
                mvn -B -DskipTests clean package
            }
        }
        stage('Test') {
            steps {
                mvn test
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './scripts/deliver.sh'
            }
        }
    }
}
