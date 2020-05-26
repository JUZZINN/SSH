pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh  mkdir html
                sh cp index.html  html/file.txt
                

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
                   sh cp   html/* /home/ec2-user/
               } 

            }
        }
    }
}
