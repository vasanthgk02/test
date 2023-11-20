properties([githubProjectProperty(displayName: '', projectUrlStr: 'https://vasanthgk02-admin@bitbucket.org/vasanthgk02/test.git/'), pipelineTriggers([githubPush()])])
pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                sh "echo hi"
            }
        }
    }
}
