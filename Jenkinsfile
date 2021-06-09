pipeline
{
agent any

  stages
  {
    stage('Clone Repo')
    {
      steps
      {
        git 'https://github.com/showmikb/aws-pcluster-create.git'
      }
    } 
    stage('Run the Config file')
    {
      steps
      {
        sh 'echo hello'
        sh 'ls -larth'
      }
    }
  }
}
