pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent ( ['sshclient']) {
    sh '''
ssh justin@192.168.43.161 echo testing connection || true
ssh-add -L
echo done running remote windows test
'''
  }
            }
        }


}
}
