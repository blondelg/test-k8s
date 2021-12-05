pipeline {
    agent any
    tools {
        'org.jenkinsci.plugins.docker.commons.tools.DockerTool' 'mydocker'
    }
    stages {
        stage('Build image') {
            steps {
                echo 'Building..'
                sh 'dockerd'
                sh "docker version"
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