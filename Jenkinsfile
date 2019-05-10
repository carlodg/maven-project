 pipeline {
    agent any

    stages{
        stage('Build'){
            steps {
                sh '''#!/bin/bash
                mvn clean package
                '''
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
