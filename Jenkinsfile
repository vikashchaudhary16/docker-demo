pipeline{
    agent any
    
    tools{nodejs "node"}
    
    stages{
        stage('Build'){
            steps{
                git branch: 'main', url: 'https://github.com/vikashchaudhary16/docker-demo.git'
            }
        }
        stage('Deploy'){
         steps{
            bat 'docker build . -t -f dockerfile.txt reactapp'
            bat 'docker run --name reactContainer -d -p 3000:80 reactapp'
         }   
        }
    }
}