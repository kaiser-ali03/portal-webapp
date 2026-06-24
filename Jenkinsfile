pipeline{
    agent any 
    stages{
        stage("Checkout"){
            steps{
                git "https://github.com/kaiser-ali03/portal-webapp.git"
            }
        }
        stage("Docker build"){
            steps{
                sh "docker build -t myapp:v1 ."
            }
        }
        stage("verify image"){
            steps{
                sh "docker images"
            }
        }
    }
}
