pipeline {
    agent any
    environment {
        KUBECONFIG = '/home/ubuntu/.kube/config'
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    git branch: 'main', credentialsId: 'your-git-credentials-id', url: 'https://github.com/ahmetcanyilmaz2022/jtest.git'
                }
            }
        }
        stage('Deploy to Kubernetes') {
            steps {
                script {
                    sh 'kubectl apply -f deployment.yaml'
                }
            }
        }
    }
}
