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
                sh 'docker build -t backend .'
            }
        }
        stage('run'){
            steps{
                sh 'docker -d -p 3004:3004 backend '
            }
        }
    }
}