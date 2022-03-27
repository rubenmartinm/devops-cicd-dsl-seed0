pipeline {
    agent {
        label('acme-aws-terraform')
    }
    stages {
        stage('Test') {
            steps {
                sh 'echo hola'
            }
        }
        stage('Is there any Terraform?') {
            steps {
                sh 'terraform init'
            }
        }
    }
}