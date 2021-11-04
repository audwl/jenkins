pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''echo "Hello World"
ls -al'''
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            sh 'sudo yum install httpd'
            sh 'sudo systemctl start httpd'
          }
        }

        stage('test-1') {
          steps {
            sh 'ls -al'
          }
        }

      }
    }

  }
}