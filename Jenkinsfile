pipeline
{
 agent any
 stages 
  {
   stage('Build') 
    {
     steps 
      {
        build 'PES1UG22CS813-1'
        sh 'g++ main.cpp -o output'
      }
    }
  stage('Test') 
    {
      steps
      {
        sh './output'
      }
    }
  stage('Deploy') {
    steps {
      ech 'deploy'
    }
  }
}
post{
failure{
error 'Pipeline failed'
}
}
}
