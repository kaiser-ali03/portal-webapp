pipeline{
    agent any 
        environment {
        IMAGE_NAME = "myapp"
        IMAGE_TAG = "${BUILD_NUMBER}"
    }
    stages{
        stage("Checkout"){
            steps{
                git "https://github.com/kaiser-ali03/portal-webapp.git"
            }
        }
        stage("Docker build"){
            steps{
                sh '''
                docker build -t $IMAGE_NAME:$IMAGE_TAG .

                '''
            }
        }
        stage("verify image"){
            steps{
                sh "docker images"
            }
        }
    }
}
