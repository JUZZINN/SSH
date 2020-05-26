pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'ls'
                sh 'cat index.html'
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
                    
                    sh 'ls /home/ec2-user/'
                  }
                }
            }
        }
    }
