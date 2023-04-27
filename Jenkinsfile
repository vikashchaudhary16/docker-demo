pipeline{
    agent any
    
    tools{nodejs "node"}
    
    stages{
        stage('Build'){
            steps{
                git branch: 'main', url: 'https://github.com/vikashchaudhary16/docker-demo.git'
                bat 'npm install'
                bat 'npm build'
            }
        }
        stage('Deploy'){
         steps{
            bat 'docker-compose up -d'
         }   
        }
    }
}