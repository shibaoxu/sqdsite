pipeline {
    agent none;
    stages {
        stage('Build') {
          agent {
            docker {
              image 'node:9.8.0-alpine' 
              args '-u root' 
            }
          }
            
          steps {
            sh 'npm config set registry http://registry.npm.taobao.org/'
            sh 'npm install' 
            sh 'npm run build'
          }
        }

        stage('Deploy') {
            agent any
            steps {
                ansiblePlaybook credentialsId: 'fbb00855-59ca-4f8c-8cfb-aa2131d4c1a1', inventory: 'ansible/hosts', playbook: 'ansible/deploy.yml', sudo: true
            }
        }
    }
}