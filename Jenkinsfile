pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent ( ['awskey']) {
    
sh cd /home/ec2-user/jenkins
sh ls

  }
            }
        }


}
}
