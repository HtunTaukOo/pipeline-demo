pipeline {
    agent any

    environment {
        IMAGE_NAME = "ht024112001/pipeline-demo"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/HtunTaukOo/pipeline-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t $IMAGE_NAME .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push $IMAGE_NAME'
            }
        }

    }
}
