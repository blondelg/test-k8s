pipeline {
    agent {
        docker { image 'hello-world' }
    }
    stages {
        stage('Build image') {
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