pipeline {
    agent {
        docker {
            image 'node:9.8.0-alpine' 
            args '-u root' 
        }
    }
    stages {
        stage('初始化') {
          steps {
            sh 'npm config set registry http://registry.npm.taobao.org/'
            sh 'npm install' 
          }
        }
        stage('Build') { 
            steps {
              sh 'npm run build'
            }
        }
        stage('归档') {
            steps {
              sh 'rm -f sqlsite.zip'
              zip zipFile: 'sqdsite.zip', dir: 'dist'
              archiveArtifacts artifacts: 'sqdsize.zip'
            }
        }
    }
}