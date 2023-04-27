pipeline{
    agent any
    
    tools{nodejs "node"}
    
    stages{
        stage('Build'){
            steps{
                git branch: 'main', url: 'https://github.com/vikashchaudhary16/ssr-demo.git'
                bat 'npm install'
                bat 'npm build'
            }
        }
        stage('Deploy'){
         steps{
            bat 'docker build . -t vchaudhary27/ssr-demo'
         }   
        }
    }
}