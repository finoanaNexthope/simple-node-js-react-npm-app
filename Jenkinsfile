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

        stage('Test') { 
            steps {
                sh './jenkins/scripts/test.sh' 
            }
        }

         stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
                sh './jenkins/scripts/kill.sh'
            }
        }
    }
}

