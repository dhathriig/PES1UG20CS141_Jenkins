pipeline{
    agent any
    stages{
      stage('Build'){
        steps{
          sh 'g++ -c PES1UG20CS141.cpp'
          sh 'g++ -o PES1UG20CS141 PES1UG20CS141.cpp
          echo 'build stage successfull'
        }
      }
      stage('Test'){
        steps{
          sh './PES1UG20CS141'
          echo 'Test stage executed successfully'
        }
      }
      stage('Deploy'){
        steps{
          echo 'Deployed successfully'
        }
      }
    }
  post{
    always{
      script{
        if(currentBuild.result=='FAILURE'){
          echo 'Pipeline Failed'
        }
      }
    }
  }
}
