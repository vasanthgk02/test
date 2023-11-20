properties([githubProjectProperty(displayName: '', projectUrlStr: 'https://github.com/vasanthgk02/test.git/'), pipelineTriggers([githubPush()])])
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
