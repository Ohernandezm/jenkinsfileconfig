String branchName = env.BRANCH_NAME
String gitCredentials = "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"
String repoUrl = "git@github.com:Ohernandezm/jenkinsfileconfig.git"

pipeline {
    agent any
    stages {
        stage('clone repos') {
          // Start Stages
  stage('Clone') {
      // Clones the repository from the current branch name
      echo 'Make the output directory'
      sh 'mkdir -p build'

      echo 'Cloning files from (branch: "' + branchName + '" )'
      dir('build') {
          git branch: branchName, credentialsId: 	gitCredentials, url: repoUrl
      }     
  }  
        }
            stage ('Invoke_pipelineA') {
                steps {
                    build job: 'Jenkinsfile', parameters: [ ]
                }
            }
    }
}
