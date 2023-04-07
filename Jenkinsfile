pipeline {
    agent any 
    tools { 
      maven 'DefaultMaven' 
    }
    stages {
        stage('Clone repo and clean it') { 
            steps {
                sh "mvn clean "
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test"
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package"
            }
        }
    }
}