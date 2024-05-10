pipeline {
    agent any
    environment {
        KUBECONFIG = '/home/ubuntu/.kube/config'
        PATH = "$PATH:/usr/local/bin"
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
