pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                git url: '' , branch: 'main'
            }
        }
        stage('build'){
            steps{
                sh 'docker build -t frontend .'
            }
        }
        stage('run'){
            steps{
                sh 'docker run -d --name frontend-container -p 3004:3004 frontend '
            }
        }
    }
}