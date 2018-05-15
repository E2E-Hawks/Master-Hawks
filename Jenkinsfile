pipeline {
  agent 
  {
    node 
    {
      label 'Susdomain'
    }

  }
  parameters
  {
      string(name: 'InstallationFolder')
      string(name: 'JreVersion')
      string(name: 'TomCatVersion')
  }
  stages {
    stage('Validation before upgrade')
     {
      steps {
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: "${params.InstallationFolder}"], [name: 'JreVersion', value: "${params.JreVersion}"], [name: 'TomCatVersion', value: "${params.TomCatVersion}"]], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
    
    stage('Upgrade') {
      
      steps {
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: '${Folder}'], [name: 'JreVersion', value: '${JreVersion}'], [name: 'TomCatVersion', value: '${TomCatVersion}']], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
    stage('Snapshot after upgrade') {
    
      steps {
        rafScript([actionBranch: 'SAS_15.1FP0', autoUpdate: true, envFile: true, envFilePath: '%OurHomeDir%\\Parameters\\KMS_271.params', killProcesses: true, linkName: 'RAF Report', rafLocation: "${SlaveRAFHome}", rafParameters: [[name: 'InstallationFolder', value: '${Folder}'], [name: 'JreVersion', value: '${JreVersion}'], [name: 'TomCatVersion', value: '${TomCatVersion}']], rdpDisconnect: true, removeFolders: false, script: 'Wait 5 sec.script', scriptBranch: 'SAS_15.1FP0'])
      }
    }
  }
}
