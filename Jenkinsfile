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
                    sh "ssh -vvv -o StrictHostKeyChecking=no -T ec2-user@52.74.83.204"
                  }
                }
            }
        }
    }
