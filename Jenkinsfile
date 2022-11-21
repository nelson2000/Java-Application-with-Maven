pipeline{
    agent any
    stages{
        stage("Code Quality checks with Sonarqube"){
            steps{
                
                script {
    
                    sh 'mvn sonar:sonar Dsonar.projectKey=JavaApp-Project Dsonar.host.url=http://34.221.65.140:9000 Dsonar.login=jenkins1'
                }
            }
            
        }
    }
    
}