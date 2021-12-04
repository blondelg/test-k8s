pipeline {
    stages {
        stage('Build image') {
            steps {
                echo 'Building..'
                app = docker.build("hello-world")
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