pipeline{
    agent any
     environment {
        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')
    }
    stages{
        stage('Terraform init'){
            steps{
                scripts{
                    sh 'terraform init'
                }
            }
        }

        stage('Terraform validate'){
            steps{
                scripts{
                    sh 'terraform validate'
                }
            }
        }
        stage('Terraform plan'){
            steps{
                scripts{
                    sh 'terraform plan -auto-approve'
                }
            }
        }
        stage('Terraform apply'){
            steps{
                scripts{
                    sh 'terraform apply -auto-approve'
                }
            }
        }
    }

}
