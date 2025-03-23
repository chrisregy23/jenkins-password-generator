pipeline{
    agent any

    parameters{
        string(name: 'MIN_LENGTH', defaultValue: '8', description: 'Specify a minimum length for your password')
        choice(name: 'MIN_NUMBER_LENGTH', choices: ['0', '1', '2'], description: 'Specify the minimum number of numerical digits you need in your password')
        choice(name: 'MIN_PUNC_LENGTH', choices: ['0', '1', '2'], description: "Specify the minimum number of special characters you need in your password")
    }

    stages{
        stage('Generate Password'){
            steps{
                script{
                    checkout scm
                    sh """
                    python3 generate-password.py <<EOF
                    ${MIN_LENGTH}
                    y
                    ${MIN_NUMBER_LENGTH}
                    y
                    ${MIN_PUNC_LENGTH}
                    EOF
                    """
                }
            }
        }
    }
}
