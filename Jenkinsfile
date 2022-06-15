pipeline {
    agent { docker { image 'alpine' } }
    tools {
        go 'go-1.18'
    }
    stages {
        stage('Compile') {
            environment {
                GO111MODULE = 'on'
                PATH = $PATH:$GOROOT
            }
            steps {
                sh 'pwd'
                sh 'ls /'
                sh 'ls /home'
                sh 'echo $GO111MODULE'
                sh 'echo $GOROOT'
                sh 'echo $PATH'
                sh 'go version'
            }
        }
    }
    post {
        success {
            echo 'Successfully'
        }
        failure {
            echo 'Failed'
        }
    }
}