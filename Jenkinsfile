pipeline {
    agent { label 'master' }
    stages {
        stage('compile') {
            agent { label 'dev' }
            steps {
                sh 'mvn clean install'
            }
        }
        stage('build') {
            agent { label 'dev' }
            steps {
                sh 'docker build -t testdev .'
            }
        }
        stage('Deploy') {
            agent { label 'prod' }
            steps {
                echo 'Deploying....'
            }
        }
    }
}