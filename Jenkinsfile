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
        stage('Tag DOcker Image'){
            steps{
                script{
                    sh 'docker tag django_demo01:$BUILD_NUMBER public.ecr.aws/e0q1u6q2/django_demo01:$BUILD_NUMBER'
                }
            }
        }
        stage('Publish into ECR'){
            steps{
                script{
                    sh 'docker push public.ecr.aws/e0q1u6q2/django_demo01:$BUILD_NUMBER'
                }
            }
        }
    }
}
