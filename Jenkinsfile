pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
 //               sh 'mvn clean package'
                  echo 'Build stage'
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
