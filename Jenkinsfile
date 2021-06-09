pipeline
{
agent any

  stages
  {
    stage('Install Pcluster')
    {
      steps
      {
       sh 'pip-3.7 install aws-parallelcluster==2.10.2 --user'
      }
    } 
    
    stage('Set Env')
    {
      steps
      {
        sh 'export PATH=/sbin:/bin:/usr/sbin:/usr/bin:~/.local/bin/'
      }
    }
    stage('Run the Config file')
    {
      steps
      {
        sh 'sudo sh createcluster.sh mycluster'
      }
    }
  }
}
