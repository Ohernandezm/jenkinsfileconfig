String branchName = env.BRANCH_NAME
String gitCredentials = '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'
String repoUrl = 'git@github.com:Ohernandezm/jenkinsfileconfig.git'
 
    stages {
        stage('Clone') {
                steps {
                // Clones the repository from the current branch name
                echo 'Make the output directory' 
                    "sh git clone  https://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@github.com/Ohernandezm/devops-products-service.git"
                }
        }
        stage ('Invoke_pipelineA') {
                steps {
                    build job: 'Jenkinsfile', parameters: [ ]
                }
        }
    } 