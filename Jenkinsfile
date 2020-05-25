pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent ( ['awskey']) {
    
sh '''
ssh ec2-user@52.74.83.204
'''

  }
            }
        }


}
}
