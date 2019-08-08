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
      
      stage('Build') {
            steps {
                sh 'npm run-script build-prod'
              rocketSend channel: '@rakuemoevi, @jmensah', message: 'test'
            }
        }
    }
}
