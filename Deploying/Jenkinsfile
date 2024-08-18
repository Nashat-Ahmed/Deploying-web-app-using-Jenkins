pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    def image = docker.build("your-dockerhub-username/webapp")
                    image.push()
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'kubectl apply -f deployment.yml'
            }
        }
    }
}

