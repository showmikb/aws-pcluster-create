pipeline
{
agent any
  stages
  {
    stage('Clone Repo')
    {
      steps
      {
       sh 'ls -alrth'
      }
    } 
    stage('Run the Config file')
    {
      steps
      {
        sh 'sudo createcluster.sh mycluster'
      }
    }
  }
}
