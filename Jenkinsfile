pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent ( ['sshclient']) {
    sh '''
ssh justin@JUZZ echo testing connection || true
ssh-add -L
echo done running remote windows test
'''
  }
            }
        }


}
}
