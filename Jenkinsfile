pipeline {
    agent any

    tools{
        maven 'M3'
    }

    stages {
        

        stage('Clean & Package'){
            steps{
                sh "mvn clean package -DskipTests"
            }
        }

        stage('Run Sonarqube') {
            environment {
                scannerHome = tool 'sonarscanner';
            }
            steps {
              withSonarQubeEnv(credentialsId: 'sonar', installationName: 'sonarqube') {
                sh "${scannerHome}/bin/sonar-scanner"
              }
            }
        }
         
       
    }
}
