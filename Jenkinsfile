pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Construyendo.... '
                withGradle {
                    sh './gradlew assemble'        
                }
            post {
                sucessfull{
                    archiveArtifacts artifacts: 'build/libs/*.jar'        
                }        
            }    
        }

        stage('Test') {
            steps {
                echo 'Testing....'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying.... '
            }
        }
    }
}