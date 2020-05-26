pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                cat 'index.html'
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
