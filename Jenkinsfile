pipeline {
 agent {
    kubernetes {
      inheritFrom 'kaniko'
    }
  }

  options {
    buildDiscarder(logRotator(numToKeepStr: '10', artifactDaysToKeepStr: '30'))
  }


  environment {
      registryCredential = 'acr-credentials'
  }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World';
                sh "cat /etc/*release";            }
        }
    }
    
}


