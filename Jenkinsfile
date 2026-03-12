pipeline {
    agent any

    environment {
        IMAGE_NAME = "ht024112001/pipeline-demo"
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main', url:  'https://github.com/HtunTaukOo/pipeline-demo.git'
            }
        }

	stage('Build Docker Image') {
            steps {
                sh 'docker build -t ht024112001/pipeline-demo .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker login -u ht024112001 -p 123456789'
                sh 'docker push ht024112001/pipeline-demo'
            }
        }
    }
}
