pipeline{
    agent any
    stages{
        stage ('1-Clone'){
            steps{
                git credentialsId: 'Git-hub-Cred', url: 'https://github.com/kiki023/Data2bbots'
            }
        }
        stage('Terraform Init'){
            steps{
                sh '/usr/local/bin/terraform init'
            }
        
        }
        stage('Terraform Plan'){
            steps{
                sh '/usr/local/bin/terraform plan'
            }
        }
        stage ('Terraform Apply'){
            steps{
                sh '/usr/local/bin/terraform apply --auto-approve'
            }
        }   
        stage ('Terraform Destroy'){
            steps{
                sh '/usr/local/bin/terraform destroy --auto-approve'
                
            }
    }
        
    }
