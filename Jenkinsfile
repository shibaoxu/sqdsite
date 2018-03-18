pipeline {
    agent {
        docker {
            image 'node:9.8.0-alpine' 
            args '-u root' 
        }
    }
    stages {
        stage('初始化编译环境') {
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
        stage('归档构建物') {
            steps {
              zip zipFile: 'sqdsize.zip', dir: 'dist'
              archiveArtifacts artifacts: 'sqdsize.zip'
            }
        }
    }
}