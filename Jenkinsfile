pipeline {
    agent {
        docker { image 'node:14-alpine' }
    }
    stages {
        stage('Build image') {
            steps {
                echo 'Building..'
                sh 'node --version'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'docker image ls'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            echo 'post always'
        }
        success {
            echo 'post success'
        }
        failure {
            echo 'post failure'
        }
    }
}