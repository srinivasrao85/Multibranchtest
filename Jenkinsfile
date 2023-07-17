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
                    error "Trying to recreate"
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
