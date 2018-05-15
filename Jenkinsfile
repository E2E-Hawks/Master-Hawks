pipeline {
  agent {
    node {
      label 'Susdomain'
    }

  }
  stages {
    stage('Validation before upgrade') {
      agent {
        node {
          label 'Susdomain'
        }

      }
      steps {
        sleep 5
      }
    }
    stage('Upgrade') {
      agent {
        node {
          label 'Susdomain'
        }

      }
      steps {
        sleep 5
      }
    }
    stage('Snapshot after upgrade') {
      agent {
        node {
          label 'Susdomain'
        }

      }
      steps {
        sleep 5
      }
    }
  }
  environment {
    InstallationFolder = 'Folder'
    TomCatVersion = 'TomCatVersion'
    JreVersion = 'JreVersion'
  }
}