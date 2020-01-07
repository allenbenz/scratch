pipeline {
    agent {
        docker {
            image 'alpine:3'
        }
    }

    stages {
        stage('Build') {
            steps {
                sh './build.sh'
                archiveArtifacts artifacts: '*.txt', fingerprint: true 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
