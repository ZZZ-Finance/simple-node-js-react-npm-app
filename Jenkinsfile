pipeline {
    environment {
        PATH = "$PATH:/usr/local/bin"
    }
    agent { label 'ci-cd' }
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
