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
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: '${Folder}'], [name: 'JreVersion', value: '${JreVersion}'], [name: 'TomCatVersion', value: '${TomCatVersion}']], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
    stage('Upgrade') {
      agent {
        node {
          label 'Susdomain'
        }

      }
      steps {
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: '${Folder}'], [name: 'JreVersion', value: '${JreVersion}'], [name: 'TomCatVersion', value: '${TomCatVersion}']], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
    stage('Snapshot after upgrade') {
      agent {
        node {
          label 'Susdomain'
        }

      }
      steps {
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: '${Folder}'], [name: 'JreVersion', value: '${JreVersion}'], [name: 'TomCatVersion', value: '${TomCatVersion}']], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
  }
  environment {
    InstallationFolder = 'Folder'
    TomCatVersion = 'TomCatVersion'
    JreVersion = 'JreVersion'
  }
}
