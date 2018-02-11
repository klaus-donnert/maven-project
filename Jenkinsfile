pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'C:\\Users\\klaus\\OneDrive\\Documents\\apache-maven-3.5.2-bin\\apache-maven-3.5.2\\bin\\mvn.cmd clean package'
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
