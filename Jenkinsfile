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
                sh "whoami";
                sh "cat /etc/passwd";
                sh "which apt || which apt-get || which apk";
            }
        }
    }
    
}

discordSend description: "Gaius Pusher Job Description \n Job Name : ${currentBuild.projectName} \n Status : ${currentBuild.currentResult}", footer: 'Footer', image: '', link: env.BUILD_URL, result: currentBuild.currentResult, scmWebUrl: '', thumbnail: '', title: 'Gaius Pusher Title', webhookURL: 'https://discord.com/api/webhooks/989880078513102858/FcY6mLAbkWAKwuODo7mN5gG34W3pvylKrTu-o2S4y6cUzCt3sQJhIihchIhBYyQx45tn'

