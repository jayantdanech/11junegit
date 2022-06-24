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

discordSend description: "Gaius Pusher Job Description \n ${currentBuild.projectName}", footer: 'Footer', image: '', link: env.BUILD_URL, result: currentBuild.currentResult, scmWebUrl: '', thumbnail: '', title: 'Gaius Pusher Title', webhookURL: 'https://discord.com/api/webhooks/989880078513102858/FcY6mLAbkWAKwuODo7mN5gG34W3pvylKrTu-o2S4y6cUzCt3sQJhIihchIhBYyQx45tn'

