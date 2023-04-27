pipeline{
    agent any
    
    tools{nodejs "node"}
    
    stages{
        stage('Build'){
            steps{
                git branch: 'master', url: 'https://github.com/vikashchaudhary16/docker-demo.git'
            }
        }
        stage('Deploy'){
         steps{
            bat 'docker-compose up -d'
         }   
        }
    }
}