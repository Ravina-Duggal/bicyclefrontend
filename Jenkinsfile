pipeline{
    agent any
    stages{
        stage('git clone'){
            steps{
                git url: 'https://github.com/Ravina-Duggal/bicyclefrontend.git' , branch: 'main'
            }
        }
        stage('build'){
            steps{
                sh 'docker build -t frontend .'
            }
        }
        stage('run'){
            steps{
                sh 'docker run -d -p 3004:3004 frontend'
            }
        }
    }
}
