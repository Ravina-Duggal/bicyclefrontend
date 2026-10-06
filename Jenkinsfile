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
<<<<<<< HEAD
                sh 'docker run -d --name frontend-container -p 4200:4200 frontend '
=======
>>>>>>> 9bedd6fed727a0ec949ff89eecadce2942cddc07
            }
        }
    }
}
