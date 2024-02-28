pipeline{
agent any
  stages{
    stage('Install Packages'){
      steps{
        tools{
        nodejs "nodejs"
      }
        script{
          sh 'yarn install'
        }
      }
    }
    
    stage('Run the app'){
      steps{
        script{
          sh 'yarn start &'
          sleep 5
        }
      }
    }
    
    stage('Visit /health route'){
      steps{
        script{
          sh 'curl http://localhost:3000/health'
        }
      }
    }

    stage('cleanup'){
      steps{
        script{
          sh 'pkill -f "node"'
        }
      }
    }

   

    
  }
  
}

