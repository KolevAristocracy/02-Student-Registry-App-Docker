pipeline{
    agent any

    tools {
        nodejs 'node18'
    }
    
    stages{
        stage("Install Dependencies"){
            steps{
                sh 'npm install'
            }
        }
        stage("Run UI Tests"){
            steps{
                sh 'npm test'
            }
        }
    }
}