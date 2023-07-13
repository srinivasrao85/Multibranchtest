pipeline{
    agent any
    environment{
        DEPLOY_TO = 'production'
    }
    stages {
        stage('Build Example') {
            when {
                allof{
                    branch 'production'
                    environment name: 'DEPLOY_TO' , value: 'production'
                }
            }
            steps{
                echo "Deploying in production"
                
            }
        }
        stage('Second stage'){
            steps{
                echo "Execute, irrespective of the condition"
            }
        }
        
    }
}
