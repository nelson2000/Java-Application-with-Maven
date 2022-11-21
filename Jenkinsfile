pipeline{
        agent {
        
    }
    stages{   

        stage{   
            
    }
    
}
}


pipeline{
    agent{
        docker {
                image 'maven:3.8.1-adoptopenjdk-11'
                args '-v /root/.m2:/root/.m2'
            }
        
    }
    stages{
        stage("Code Quality Analysis"){
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
