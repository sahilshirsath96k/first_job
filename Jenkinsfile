pipeline {
    agent any tests
    
    parameters {
    string(name: 'VERSION', defaultValue: '1.0', description: 'Version to deploy')
    choice(name: 'ENVIRONMENT', choice: ['staging', 'production'], description: 'Target')
    booleanParam(name: 'SKIP_TESTS', defaultValue: false, description: 'Skip tests?')
    }
    
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
    }
}
