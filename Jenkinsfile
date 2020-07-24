pipeline {
    agent { label 'Slave1' }
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
                 sh 'cd /home/ubuntu/'
                 sh 'sudo docker-compose up -d'                 
                  sh 'sudo ls -l'
            }
        }
      }
    

 post { 
        always { 
            echo 'Hello'
        }
       success {
           echo 'Build was successfull'
         }
    }
}
