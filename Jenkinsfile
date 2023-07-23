pipeline{
    agent any
    stages{
        stage('build'){
            steps{
                echo "Build completed successfully"
            }
        }
    }
    post {
        success {
           echo "Success"
        }
        failure {
           echo "Failure"
        }
        always {
           echo "Always called."
        }
    }
}
