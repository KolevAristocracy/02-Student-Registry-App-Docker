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
        stage("Testing"){
            failFast true
            parallel {
                stage("Run npm security"){
                    steps{
                        sh 'npm audit'
                    }
                }

                stage("Run UI Tests"){
                    steps{
                        sh 'npm test'
                    }
                }
            }
        }
    }
}