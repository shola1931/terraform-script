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

        stage('Manual Check') {
            steps {
                input message: 'Apply this Terraform?', ok: 'Yes'
            }
        }

         stage('Apply Terraform') {
            steps {
                sh 'terraform apply --auto-approve'
            }
        }
    }

}