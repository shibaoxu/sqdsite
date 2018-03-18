pipeline {
    agent {
        docker {
            image 'node:9.8.0-alpine' 
            args '-u root' 
        }
    }
    stages {
        stage('Init Env') {
          steps {
            sh 'npm config set registry http://registry.npm.taobao.org/'
            sh 'npm install' 
          }
        }
        stage('Build') { 
            steps {
              sh 'npm run build'
              archiveArtifacts artifacts: 'dist/**'
            }
        }
    }
}