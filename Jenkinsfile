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


        script{
          sh 'pip-3.7 install aws-parallelcluster==2.10.2 --user'
        }
      }
    } 
    

    stage('Create or Update Cluster with the Config file')
    {
      steps
      {
        script 
        {
            try 
            {
               sh """#!/bin/bash
            GIT_COMMIT_ID=`git rev-parse HEAD`
            echo "The value is \$GIT_COMMIT_ID"
            FILE_NAME=`git diff-tree --no-commit-id --name-only -r \$GIT_COMMIT_ID`
            echo "\$FILE_NAME"
            `pcluster create -c config \$FILE_NAME`
            """
              
            } 
            catch (Exception e) 
            {
                echo 'Exception occurred: ' + e.toString()
                sh 'pcluster update -c config tesla -y'
            }
        }
        
      }
    }
  }
}
