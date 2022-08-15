pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               sh """
               echo "Building ReadMe file"
               """
           }
       }
      stage('Deploy Code') {
          steps {
               sh "./deploy"
               echo "Deploying Code"
               """
          }
      }
   }
}
