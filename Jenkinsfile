pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World';
            }
        }
    }
    
}

discordSend description: "Gaius Pusher Job Description \n Job Name : ${currentBuild.projectName} \n Status : ${currentBuild.currentResult}", footer: 'Footer', image: '', link: env.BUILD_URL, result: currentBuild.currentResult, scmWebUrl: '', thumbnail: '', title: 'Gaius Pusher Title', webhookURL: '*'

