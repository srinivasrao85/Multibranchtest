pipeline{
    agent any
    parameters{
        string (
            name: 'USR_NAME',
            defaultValue: 'Srini',
            description: 'Do enter your name'
        )
    }
    stages{
        stage('welcome'){
            steps{
                echo "echo welcome ${params.USR_NAME}"
            }
        }
    }
}
