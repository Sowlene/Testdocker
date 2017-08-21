pipeline {
  agent any
  stages {
    stage('Welcome') {
      steps {
        parallel(
          "Welcome": {
            echo 'Welcome'
            dir(path: '/var/lib/jenkins/workspace/Sowlene_Docker_Tr_master-BKNB6FCY5LJARIWM7QM33SLIQXAUMZFX6H7O3WOAIWZETDJQEIOQ/debian_Dev/') {
              sh 'pwd && who && ls -Shal #l not pass'
            }
            
            
          },
          "First": {
            sh 'pwd && who && ls -Shal #l not pass'
            
          }
        )
      }
    }
    stage('Change Directory') {
      steps {
        sh 'cd Debian_Dev/ && ls -Shal'
      }
    }
    stage('Build Docker Image') {
      steps {
        parallel(
          "Build Docker Image": {
            sh 'ls -lhS /var/run/ | grep docker.sock'
            
          },
          "Build": {
            sh 'pwd && docker build -t solene/installtv2 .'
            
          }
        )
      }
    }
    stage('End') {
      steps {
        echo 'End '
      }
    }
  }
}