pipeline {
    agent any

    stages {
        
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t django_demo01:$BUILD_NUMBER .'
                 }

            }
        }
    }
}
