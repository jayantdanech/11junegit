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
                sh "cat /etc/*release";
                discordSend description: "Gaius Pusher Job Description \n Job Name : ${currentBuild.projectName} \n Status : ${currentBuild.currentResult}", footer: 'Footer', image: '', link: env.BUILD_URL, result: currentBuild.currentResult, scmWebUrl: '', thumbnail: '', title: 'Gaius Pusher Title', webhookURL: '*'
            }
        }
    }
    
}


