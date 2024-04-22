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
                stage("test") {
            steps {
                   dir('Frontend') {
               bat "npm test" 
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
