pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Construyendo.... '
                withGradle {
                    sh './gradlew assemble'        
                }
                
            }
        }
        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'builds/libs/*.jar'
            }
        }
    }
}