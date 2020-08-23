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
                sh 'chmod +x ./build.sh'
                sh './build.sh' 
            }
        }
    }
}
