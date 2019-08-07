pipeline {
    agent {
        docker {
            image 'node' 
        }
    }
    stages {
        stage('Npm install') { 
            steps {
                sh 'npm install'
            }
        }
      stage('test unit') { 
            steps {
                sh 'npm run-script test'
            }
        }
      stage('Build') { 
            steps {
                sh 'npm run-script build-prod'
            }
        }
    }
}
