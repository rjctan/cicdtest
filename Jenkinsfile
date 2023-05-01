pipeline {
    agent { label 'kubeagent' }
     options {
        buildDiscarder(logRotator(numToKeepStr:'5'))
    }
    stages {   
        stage('clean workspaces') { 
            steps {
              cleanWs()
              sh 'env'
            }
        }
        stage("git clone code terraform") {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: 'master']], 
                    doGenerateSubmoduleConfigurations: false, 
                    extensions: [],
                    submoduleCfg: [], 
                    userRemoteConfigs: [[credentialsId: 'test', url: 'https://github.com/rjctan/cicdtest.git']]
                ])
            }
        }
        stage("git clone code terraform") {
            steps {
                sh '''
                  echo "hola"
                  ''''
                )
            }
        }
    }
}
