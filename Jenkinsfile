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
                 
                 sh 'sudo mvn package'
              
            }
        }

        stage('Docker-compose build') {
           steps {
                 echo 'Build images and run conatiners using docker files'
                 sh 'cd /home/ubuntu/Git/ALL'
                 sh 'sudo docker-compose up -d'
     
      }
    }

    stage('Ansible-Task') {
           steps {
                 echo 'Move the artifacts to the slave server'
                 sh 'cd /home/ubuntu/Git/ALL'
                 sh 'sudo ansible-playbook Move.yaml'

      }
    }

}

 post {
        always {
            echo 'Print this message always'
        }
       success {
           echo 'Build was successfull'
         }
       failure {
           echo 'Build was unstable'
         }

    }
}



