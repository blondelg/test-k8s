pipeline {
    stage('Initialize'){
            def dockerHome = tool 'mon-docker'
            env.PATH = "${dockerHome}/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh "pwd"
                sh "ls -l"
                sh "docker -v"
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