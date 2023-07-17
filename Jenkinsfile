pipeline{
    agent any
    stages{
        stage('Build'){
          steps{
            echo "Building maven apps"
          }
        }
        stage('scans'){
          parallel {
            stage('sonar'){
                steps{
                   echo "****performing sonar scans ******"
                   sleep 10
             }
            }
            stage('fortify'){
                steps{
                  echo "*****fortify scan scans *****"
                  sleep 10
                }
            }
            stage('Trivy'){
                steps{
                    echo "**********container images scan*******"
                    error "Trivia should fail"
                    sleep 10
                }
            }
            
          }  
        
       } 
       stage('Deploy'){
        steps{
            echo "Deploying to env"
        }
       } 
    }   
}
