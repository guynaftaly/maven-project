pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                sh '/opt/apache-maven-3.6.3/mvn/bin clean package'
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