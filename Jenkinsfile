pipeline {
    agent any
    stages {
        stage('git repo clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Ashish-rajpoot/my-movie-plan.git'
            }
        }
        // stage('clean') {
        //     steps {
        //         sh "mvn clean"
        //     }
        // }
        // stage('package') {
        //     steps {
        //         sh "mvn package"
        //     }
        // }
        stage('docker version') {
            steps {
                sh "docker compose version"
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
