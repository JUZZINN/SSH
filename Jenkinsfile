pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent (credentials: ['my-node-access']) {
                  sh " ls /home/ec2-user"
                    
                  
  }
            }
        }


}
}
