pipeline {
    agent none
    stages {
            stage('test') {
            agent any
            steps {
                sshagent (credentials: ['my-node-access']) {
                  sh "touch newffile"
                    
                  
  }
            }
        }


}
}
