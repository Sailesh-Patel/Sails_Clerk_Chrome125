pipeline {
    agent any
    stages {
        stage("npm install") {
            steps {
                dir('Frontend') {
               bat "npm install" 
                }
            }
        }
  stage("npm run build") {
            steps {
                dir('Frontend') {
               bat "npm run build" 
                }
            }
        }
    }
    
    post {
          always {
               echo "pipeline concluded."
          }
          success{
               echo "all stages executed with success."
              dir('Frontend') {
               bat 'npm start'
              }
          }
    }
}
