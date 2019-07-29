pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Npm i') { 
            steps {
                sh 'npm install'
            }
        }
      stage('Build2') { 
            steps {
                sh 'npm run-script build-prod'
            }
        }
    }
}
