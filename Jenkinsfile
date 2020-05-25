pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent ( ['awskey']) {
    
sh ls /home/ec2-user/jenkins


  }
            }
        }


}
}
