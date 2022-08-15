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
               sh "./deploy2"
             
               sh "mkdir /var/lib/jenkins/live/production2"
               sh "cd /var/lib/jenkins/live/production2"

               sh " git clone https://github.com/mohammadfazeelDevopsSalsoft/DemoNodeProject/"
               sh   "cd /var/lib/jenkins/live/production2/DemoNodeProject"
               sh " npm install" 
               sh " pm2 start 'node app.js' "
               echo "Deploying Code" 
         
          }
      }
   }
}
