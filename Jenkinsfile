pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh  mkdir artifact
                    cp *.html artifact/index.html

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
