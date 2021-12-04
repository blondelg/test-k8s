pipeline {
    agent {
        docker { image 'hello-world:latest' }
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "pwd"
                sh "ls -l"
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