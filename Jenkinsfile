pipeline{
    agent any
     environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
    stages{
        stage('Terraform init'){
            steps{
                script{
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform validate'){
            steps{
                script{
                    sh 'terraform validate'
                }
            }
        }
        stage('Terraform plan'){
            steps{
                script{
                    sh 'terraform plan -auto-approve'
                }
            }
        }
        stage('Terraform apply'){
            steps{
                script{
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }

}
