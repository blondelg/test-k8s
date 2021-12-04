pipeline {
    agent any
    stages {
        stage('Build image') {
            agent {
                docker { image 'hello-world' }
            }
            steps {
                echo 'Building..'
                sh 'ls -l'
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