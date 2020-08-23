pipeline {
    environment {
        PATH = "$PATH:/usr/local/bin"
    }
    agent { none }
    stages {
        stage('Build') { 
            steps {
              withEnv(["PATH=$PATH:~/.local/bin"]){
                sh "chmod +x ./build.sh"
                sh "./build.sh"
              }
            }
        }
    }
}
