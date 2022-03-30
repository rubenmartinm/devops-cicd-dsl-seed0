pipeline {
    agent {
        label('acme-gcp-terraform')
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
                sh 'terraform --version'
            }
        }
        stage('Is there any gcp sdk?') {
            steps {
                sh 'gcloud --version'
            }
        }
    }
}