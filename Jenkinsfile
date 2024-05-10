pipeline {
    agent any
    environment {
        KUBECONFIG = '/home/ubuntu/.kube/config'
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ahmetcanyilmaz2022/jtest.git'
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
