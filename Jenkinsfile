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


        
       
    }
}
