pipeline {
    agent any

    tools {
        terraform 'terraform'
    }

    stages {

        stage('Clone Code') {
            steps {
                git branch: 'master',
                url: 'https://github.com/mnayini/terraform-jenkins.git'
            }
        }

        stage('Terraform Version') {
            steps {
                sh 'terraform version'
            }
        }

        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Terraform Validate') {
            steps {
                sh 'terraform validate'
            }
        }
    }
}
