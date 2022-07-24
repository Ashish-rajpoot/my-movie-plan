pipeline {
    agent any
    stages {
        stage('git repo clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashish-rajpoot/my-movie-plan.git'
            }
        }
       
        stage('docker compose build') {
             steps {
                 sh "docker compose build"
             }
        }

        stage('docker compose start') {
             steps {
                 sh "docker compose up -d"
             }
        }
    }
}
