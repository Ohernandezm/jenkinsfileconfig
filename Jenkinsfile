pipeline {
    agent any
    stages {
        stage('clone repos') {
            steps { 
                // clones repo1 in ${WORKSPACE}/repo1
                dir('repo1') {
                    checkout([
                    $class: 'GitSCM',
                    branches: [[name: "$GIT_BRANCH" ]],
                    extensions: [[$class: 'PruneStaleBranch']],
                    userRemoteConfigs: [[
                        url: 'git@github.com:Ohernandezm/devops-products-service.git',
                    ]]
                ])
                }
            }
            stage ('Invoke_pipelineA') {
                steps {
                    build job: 'Jenkinsfile', parameters: [ ]
                }
            }
        }
    }
}
