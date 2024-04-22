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
               bat "npm test" 
            
            }
        }

    }
    
    post {
          always {
               echo "pipeline concluded."
          }
          success{
               echo "all stages executed with success."
               bat 'npm start'
          }
    }
}
