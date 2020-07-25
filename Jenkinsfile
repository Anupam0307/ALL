pipeline {
    agent any
    stages {
        stage('Git Checkout') {
           steps {
                 echo 'Git checkout'
                 git 'https://github.com/Anupam0307/ALL.git'
              
            }
        }
     stage('Build Artifacts') {
           steps {
                 echo 'Build Artifacts'
                 sh 'cd /home/ubuntu/beps10'
                 sh 'sudo mvn package'
              
            }
        }

        stage('Docker-compose build') {
           steps {
                 echo 'Build images and run conatiners using docker files'
                 sh 'docker-compose up -d'
     
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



