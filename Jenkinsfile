pipeline {
    agent any

    tools {
        nodejs 'NodeJS 22'  // nom que vous avez configuré
    }
    
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}

