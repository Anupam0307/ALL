pipeline {
    agent {
    label 'Slave1' }
    stages {
        stage('Git Checkout') {
           steps {
                 echo 'Git checkout'
                git 'https://github.com/Anupam0307/ALL.git'
                sh 'sudo touch 58.txt'
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

