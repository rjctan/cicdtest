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
                sh '''
                  echo "hola"
                  ''''
                )
            }
        }
    }
}
