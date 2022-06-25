pipeline {
    agent any

    stages {
        stage('Initialize Terraform') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Apply Terraform') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }

}