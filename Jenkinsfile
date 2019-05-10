 pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bash 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving..'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
    }
}
