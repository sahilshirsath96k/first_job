pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building'
            }
        }
        stage('Tests') {
            parallel {
                stage('Unit') { steps { sh 'echo Running unit tests' } }
                stage('Integration') { steps { sh 'echo Running integration tests' } }
            }
        }
    }
}
