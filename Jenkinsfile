pipeline{
    agent any
    
    tools{nodejs "node"}
    
    stages{
        stage('Build'){
            steps{
                docker version
                docker info
                docker compose version
                git branch: 'main', url: 'https://github.com/vikashchaudhary16/docker-demo.git'
            }
        }
        stage('Deploy'){
         steps{
            bat 'docker-compose up -d'
         }   
        }
    }
}