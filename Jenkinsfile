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
             rocketSend channel: '@rakuemoevi, @jmensah', message: 'test'
         }
      stage('Build') {
            steps {
                sh 'npm run-script build-prod'
            }
        }
    }
}
