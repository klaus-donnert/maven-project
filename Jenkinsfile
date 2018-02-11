pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'mvn.bat clean package'
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
