pipeline {
    agent { label 'master' }
    stages {
        stage('Build') {
            agent { label 'dev' }
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            agent { label 'staging' }
            steps {
                echo 'Testing..'
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