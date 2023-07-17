pipeline{
    agent any
    environment{
        DEPLOY_TO = 'srini'
    }
    stages{
        stage('Build example'){
            steps{
                echo "This is build stage"
            }

        } 
        stage('Git'){
            when{
                anyOf{
                    expression{
                    BRANCH_NAME ==~ /(production|staging)/
                    }
                }
                environment name: 'DEPLOY_TO' , value: 'srini'
            }
            steps{
                echo "Deploying in non prod"
            }
        }
        stage('Prod deploy'){
            when{
                buildingTag()
            }
            steps{
                echo " Deploying in Prod"
            }
        }
           
    }
}
