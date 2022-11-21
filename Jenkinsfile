pipeline{
    agent any
    stages{
        stage("Code Quality checks with Sonarqube"){

            docker {
                 'image: openjdk:11'
            }
            steps{
                
                script {
                withSonarQubeEnv(credentialsId: 'sonar-cred1') {
                sh 'mvn clean package sonar:sonar'
                }
            }
            
        }
    }
    
}
}