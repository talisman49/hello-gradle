pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'make' 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'make check' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                sh 'make publish'
            }
        }
    }
}