pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'Now building'
                bash 'gradlew build war'
                }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}