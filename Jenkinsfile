
pipeline {
    agent any
    stages {
        stage('CleanUp de workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Cloner le Github') {
            steps {
                 git branch: 'main', url: 'https://github.com/aissatou00/depotOnline26.git'
            }
        }

        stage('installer Docker') {
            steps {
                 sh 'sudo apt-get update'
                 sh 'sudo apt -get innstall apt-transport-https ca-certificates curl software-properti'
                 sh 'sudo apt-get install docker.io' 
                 sh 'sudo apt update'
                 sh 'sudo chmod 666 /var/run/docker.sock'
                 sh 'sudo usermod -aG docker $USER'
                 sh 'sudo systemctl restart docker.service'
            }
        }
        
    }
}


