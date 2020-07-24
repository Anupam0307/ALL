pipeline {
    agent any
    stages {
        stage('Git Checkout') {
           steps {
                 echo 'Git checkout'
                 git 'https://github.com/Anupam0307/ALL.git'
              
            }
        }
     stage('Docker-compose build') {
           steps {
                 echo 'Build images and run conatiners using docker files'
                 sh 'cd /home/ubuntu/Git/ALL'
                 sh 'sudo docker-compose up -d'                 
                  sh 'sudo ls -l'
            }
        }
      }
    }
