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
               sh "mkdir /var/lib/jenkins/live/production/
               cd /var/lib/jenkins/live/production/
#mkdir /var/lib/jenkins/live/production/DemoNodeProject
git clone https://github.com/mohammadfazeelDevopsSalsoft/DemoNodeProject/
cd /var/lib/jenkins/live/production/DemoNodeProject
npm install
pm2 start 'node app.js'"
               echo "Deploying Code"
               """
          }
      }
   }
}
