
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
                 sh 'sudo apt purge docker* -y' 
                 sh 'sudo apt autoremove docker.io docker-compose -y'
                 sh 'sudo apt-get update'
                 sh 'sudo apt-get install apt-transport-https ca-certificates curl software-properties-common -y'
                 sh 'sudo apt-get install docker.io -y' 
                 sh 'sudo apt update'
                 sh 'sudo chmod 666 /var/run/docker.sock'
                 sh 'sudo usermod -aG docker $USER'
                 sh 'sudo systemctl restart docker.service'
            }
        } 

        stage('build image docker') {
           steps {
                  script{
                sh 'sudo docker image rm -f "mynginx:latest"'
                sh 'sudo docker build -t "mynginx:latest" .'
                sh 'sudo docker image ls'
                     }
            }    
        }

        
    }
}


