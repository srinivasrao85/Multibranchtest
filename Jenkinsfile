pipeline{
    agent any
    parameters{
        string (
            name: 'USR_NAME',
            defaultValue: 'Srini', 
            description: 'Do enter your name'
        )
        booleanParam(
            name: 'SRE_APPROVED',
            defaultValue: true,
            description: 'Is SRE approval taken for this release'
        )
    }
    stages{
        stage('welcome'){
            steps{
                echo "echo welcome ${params.USR_NAME}"
                echo "Status of approval ${params.SRE_APPROVED}"
            }
        }
    }
}
