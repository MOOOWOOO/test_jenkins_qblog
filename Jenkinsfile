node {
  stage("scm") {
    checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '4e66c1b1-91e1-45f4-9e8f-12722adb1f4f', url: 'git@github.com:MOOOWOOO/test_jenkins_qblog.git']]])
  }
  stage("ssh transfer") {
    script {
      sshPublisher(publishers: [sshPublisherDesc(configName: 'ser2', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '''conda deactivate
conda activate flask_test
python3 /opt/tf/app.py''', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/opt/tf', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
  }
}