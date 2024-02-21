pipeline{
    agent any
    environment {
        CLOUDSDK_CORE_PROJECT='thematic-carver-414815' 
        
  }
    stages{

        stage('Git checkout'){
            steps{
                git branch: 'main', url: 'https://github.com/vijkr/jenkin.git'
            }
        }
        stage('Initialize'){
            steps{
                
                sh 'terraform init'
            
            }
        }
        stage('Plan'){
            steps{
                
                sh 'terraform plan'
            
            }
        }
        stage('apply'){
            steps{
                
                sh 'terraform apply -auto-approve'
        stage ('remove')
            setps {

                sh 'terraform destroy -auto-approve'
                    
                
                }
            
            }
        }
    }
}
