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
        stage('delete old container'){
            steps{
                sh 'docker stop frontend-container || true'
                sh 'docker rm frontend-container || true'
                // hello
            }
        }
        stage('run'){
            steps{

                sh 'docker run -d --name frontend-container -p 4200:4200 frontend '

            }
        }
    }
}
