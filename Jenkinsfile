pipeline {
    agent any

    parameters {
        string(
            name: 'VERSION',
            defaultValue: '1.0',
            description: 'Version to deploy'
        )

        choice(
            name: 'ENVIRONMENT',
            choices: ['staging', 'production'],
            description: 'Target'
        )

        booleanParam(
            name: 'SKIP_TESTS',
            defaultValue: false,
            description: 'Skip tests?'
        )
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Tests') {
            parallel {
                stage('Unit') {
                    steps {
                        sh 'echo Running unit tests'
                    }
                }
                stage('Integration') {
                    steps {
                        sh 'echo Running integration tests'
                    }
                }
            }
        }
    }
}
