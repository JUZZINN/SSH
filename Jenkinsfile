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
                sshagent (['my-local-system']) {
                    sh 'scp -vvv index.html  root@192.168.43.161://home/justin/'
                
                  }
                }
            }
        }
    }
