pipeline
{
agent any

  stages
  {
    stage('Clone Repo')
    {
      steps
      {
        sh '$pwd'
        sh 'git clone https://github.com/showmikb/aws-pcluster-create.git'
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
