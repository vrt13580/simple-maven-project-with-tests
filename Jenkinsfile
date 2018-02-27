pipeline {
  agent any
  stages {
    stage('Stage1') {
      parallel {
        stage('Stage1') {
          agent {
            node {
              label 'slave1'
            }
            
          }
          steps {
            echo 'Blue Pipeline Step 1'
          }
        }
        stage('Stage2') {
          agent {
            node {
              label 'slave1'
            }
            
          }
          steps {
            archiveArtifacts '**/target/*'
          }
        }
      }
    }
  }
}