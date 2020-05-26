pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                ls 
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
                    sh 'scp index.html  ec2-user@52.74.83.204:/home/ec2-user'
                  }
                }
            }
        }
    }
