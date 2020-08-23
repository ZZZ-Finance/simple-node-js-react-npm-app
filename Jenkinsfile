pipeline {
    environment {
        PATH = "$PATH:/usr/local/bin"
    }
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3000' 
        }
    }
    stages {
        stage('Build') { 
            steps {
              withEnv(["PATH=$PATH:~/.local/bin"]){
                sh "bash test.sh"
              }
            }
        }
    }
}
