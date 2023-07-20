pipeline{
    options{
        buildDiscarder(logRotator(numToKeepStr: '5'))
    }
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
        choice(
            choices: 'Regular\nHotfix',
            description: "What sort of Release is this, regular or hotfix? ",
            name: 'Release'
        )
        text(
            name: 'Notes',
            defaultValue: 'Enter Release notes',
            description: 'Do enter the description'
        )
        credentials(
            name: 'mycredentials',
            description: "myCredentials",
            required: true
        )
    }
    stages{
        stage('welcome'){
            steps{
                echo "welcome ${params.USR_NAME}"
                echo "Status of approval ${params.SRE_APPROVED}"
                echo "This is a ${params.Release}"
            }
        }
    }
}
