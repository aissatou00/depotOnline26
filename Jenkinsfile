
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
                sh 'git clone https://github.com/aissatou00/depotOnline26.git
            }
        }
        
    }
}