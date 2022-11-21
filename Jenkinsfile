pipeline{
    agent{
        docker {
                image 'maven:3.8.1-adoptopenjdk-11'
                args '-v /root/.m2:/root/.m2'
            }
        }
    stages{
        stage("Scan"){
            steps{
                    script {
                            withSonarQubeEnv(credentialsId: 'sonar-cred1') {
                            sh 'mvn clean sonar:sonar'
                            }



                        }
            
                }


            }
           
	stage('Quality Gate') {
		steps {
			
			
                            //timeout(time: 1, unit: 'HOURS') {
		                    //def qg = waitForQualityGate()
		                    //if (qg.status != 'ok') {
		                    //error "Pipeline aborted due to quality gate failure: ${qg.status}"
		                    //}
                            //}
			
			timeout(time:5, unit: 'MINUTES') {
	 		waitForQualityGate abortPipeline: true
			}
		}

	
	}  
	    
	    
        }
    }
