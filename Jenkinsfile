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
                ansiblePlaybook credentialsId: '67aa5915-e383-4e88-bd80-d684b93d5050', inventory: 'ansible/hosts', playbook: 'ansible/deploy.yml', sudo: true
            }
        }
    }
}