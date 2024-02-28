pipeline{
agent any
  tools{
        nodejs "nodejs"
      }
  stages{
    stage('Install Packages'){
      steps{
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
    
  
    stage('cleanup'){
      steps{
        script{
          sh 'pkill -f "node"'
        }
      }
    }   
  }
  
}

