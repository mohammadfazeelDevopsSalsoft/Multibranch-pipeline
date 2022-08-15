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
               sh "mkdir /var/lib/jenkins/live/production"
               sh "cd /var/lib/jenkins/live/production"

               sh " git clone https://github.com/mohammadfazeelDevopsSalsoft/DemoNodeProject/"
               sh   "cd /var/lib/jenkins/live/production/DemoNodeProject"
               sh " npm install" 
               sh " pm2 start 'node app.js' "
               sh " echo "Deploying Code"
         
          }
      }
   }
}
