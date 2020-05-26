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
                    sh 'ssh -o StrictHostKeyChecking=no -l ec2-user@52.74.83.204'
                    sh 'ls /home/ec2-user/'
                  }
                }
            }
        }
    }
