pipeline {
    agent {
        label('acme-aws-terraform')
    }
    options { 
        disableConcurrentBuilds()   // evita que dos pipelines corran a la vez (por ejemplo para no corromper los estados de terraform)
        timeout(time: 10, unit: 'MINUTES')
        timestamps()
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