pipeline {
  agent {
    node {
      label 'ThirdParty_KMS'
    }

  }
  stages {
    stage('Validation before upgrade') {
      steps {
        sleep 5
      }
    }
    stage('Upgrade') {
      steps {
        sleep 5
        sleep 5
      }
    }
    stage('Take snapshot') {
      steps {
        sleep 5
      }
    }
  }
  parameters {
    string(name: 'InstallationFolder', defaultValue: 'JRE7_181_Tomcat7.0.86-15.181.86.32', description: 'Enter kit folder location \\10.161.124.3\\Team Folders\\Sustaining E2E (Hawks)\\3rd PARTY\\In Testing\\KMS kits\\KMS 3.2.1\\JRE7_181_Tomcat7.0.86-15.181.86.32')
    string(name: 'JreVersion', defaultValue: '1.7.0_181', description: 'jave version 1.7.0_X')
    string(name: 'TomCatVersion', defaultValue: '4.0.48', description: 'TomCat version')
  }
}