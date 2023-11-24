pipeline {
    agent any
    stages {
        stage('remove') { 
            steps {
                echo 'sudo docker compose -f anotation-frontend-dockercompose.yml down'
            }
        }
        stage('build') { 
            steps {
                echo 'sudo docker compose -f anotation-frontend-dockercompose.yml up -d'
            }
        }
        stage('deploy') { 
            steps {
                echo 'deploying the application'
            }
        }
    }
}