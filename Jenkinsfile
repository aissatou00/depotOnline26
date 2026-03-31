
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
        
    }
}