pipeline
{
agent any
environment
  {
    PATH='/sbin:/bin:/usr/sbin:/usr/bin:~/.local/bin/'
  }
  stages
  {
    stage('Install Pcluster if not present')
    {
      steps
      {
        environment {
                GIT_COMMIT_ID=''
            }

        script{
       sh 'pip-3.7 install aws-parallelcluster==2.10.2 --user'
        env.GIT_COMMIT_ID =  sh ' git rev-parse HEAD'
        sh ' echo ${env.GIT_COMMIT_ID}'
         sh 'git diff-tree --no-commit-id --name-only -r ${env.GIT_COMMIT_ID}'
        }
      }
    } 
    

//     stage('Create or Update Cluster with the Config file')
//     {
//       steps
//       {
//         script 
//         {
//             try 
//             {
//                 sh 'echo  ${env.GIT_COMMIT}'
//                 sh 'pcluster create -c config tesla'
//             } 
//             catch (Exception e) 
//             {
//                 echo 'Exception occurred: ' + e.toString()
//                 sh 'pcluster update -c config tesla -y'
//             }
//         }
        
//       }
//     }
  }
}
