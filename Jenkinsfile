pipeline {
    
    agent any

    stages {

        stage("Build Docker Image") {
            steps {
                //sh "echo 'Contrução da Imagem'"
                script {
                    dockerapp = docker.build("franciscos/kube-news:v1", "-f ./src/Dockerfile", "./src")
                }
            }
        }

        stage("Push Docker Image") {
            steps {
                sh "echo 'Envio da Imagem'"
            }
        }

        stage("Deploy no kubernetes") {
            steps {
                sh "echo 'Deploy no Kubernetes'"
            }
        }

    }
}