pipeline {
    agent { docker { image 'nsis:v3.08' } }
    tools {
        go 'go-1.18'
    }
    stages {
        stage('Compile') {
            steps {
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