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
        sh 'ls -larth /var/lib/jenkins/.local/bin/'
        sh './var/lib/jenkins/.local/bin/pcluster create -c config -r us-east-1 myclust'
      }
    }
  }
}
