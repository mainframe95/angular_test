pipeline {
    agent {
        docker {
            image 'node' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Npm install') { 
            steps {
                sh 'npm install'
            }
        }
      stage('Build2 develop') { 
            steps {
                sh 'npm run-script build-prod'
            }
        }
    }
}
