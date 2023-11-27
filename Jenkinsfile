pipeline {
    agent any
    stages {
        stage('remove') { 
            steps {
                sh '''
                echo 'docker remove and path-------------------------'
                pwd
                docker compose -f anotation-frontend-dockercompose.yml down
                docker rm -f anotaion-tool-frontend
                '''
            }
        }
        stage('build') { 
            steps {
                sh '''
                docker compose -f anotation-frontend-dockercompose.yml up -d
                '''
            }
        }
        stage('deploy') { 
            steps {
                sh '''
                docker ps
                '''
            }
        }
    }
}