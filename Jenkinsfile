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
                rocketSend channel: 'general', message: 'My message', rawMessage: true
             }
         }
      stage('Build') {
            steps {
                sh 'npm run-script build-prod'
            }
        }
    }
}
