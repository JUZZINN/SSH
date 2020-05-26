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
                sshagent (['my-node-access']) {
                    sh 'scp -vvv index.html   ec2-user@52.74.83.204:/home/ec2-user'
                
                  }
                }
            }
        }
    }
