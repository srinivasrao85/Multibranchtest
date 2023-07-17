pipeline{
    agent any
    stages{
        stage('Build'){
          steps{
            echo "Building maven apps"
          }
        }
        stage('scans'){
          Parallel {
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
                staeps{
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
