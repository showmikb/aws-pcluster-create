pipeline
{
agent any
environment
  {
    PATH='/sbin:/bin:/usr/sbin:/usr/bin:/home/ec2-user/.local/bin'
  }  

  stages
  {
    stage('Clone Repo')
    {
      steps
      {
       sh 'env'
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
