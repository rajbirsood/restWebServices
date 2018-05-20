pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                echo 'Now building'
                bat 'gradlew build war'
                }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/*.war'
                }
            }
        }
    }
}