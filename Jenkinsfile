pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'index.html'
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
                    sh 'cp index.html  /home/ec2-user'
                  }
                }
            }
        }
    }
