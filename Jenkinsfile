pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh  mkdir artifact
                    cp index.html artifact/

            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
               sshagent (credentials: ['my-node-access']) {
                   sh cp  artifact/* /home/ec2-user
               } 

            }
        }
    }
}
