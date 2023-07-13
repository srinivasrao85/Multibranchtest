pipeline{
    agent any
    stages {
        stage('Build Example') {
            when {
                expression {
                    BRANCH_NAME ==~ /(production|staging)/
                }     
            }
            steps{
                echo "Deploying in jenkins"
                
            }
        }
        stage('Second stage'){
            steps{
                echo "Execute, irrespective of the condition"
            }
        }
        
    }
}
