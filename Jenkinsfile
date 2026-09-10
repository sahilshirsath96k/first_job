pipeline {
    agent any
    stages {
        
        stage('Build') {
            steps {
                echo 'Builing the Project' 
            }
        }
        
        stage('Test') {
            steps {
                echo 'Testing the Build'
            }
        }
    }
    
    post {
        success() {
            echo 'succeded'
        }
    }
}
