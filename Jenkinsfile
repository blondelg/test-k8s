pipeline {
    agent any
    stages {
        stage('Build image') {
            app = docker.build("hello-world")
            steps {
                echo 'Building..'
                sh "pwd"
                sh "ls"
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