properties([githubProjectProperty(displayName: '', projectUrlStr: 'https://github.com/vasanthgk02/test.git/'), pipelineTriggers([githubPush()])])
pipeline {
    
    agent any
    triggers {
        githubPush(
            branches: [
                // Trigger on pull requests from test to develop or test to release
                [pattern: 'test:develop'],
                [pattern: 'test:release']
            ]
        )
    }
    stages {
        stage("Build") {
            steps {
                sh "echo hi"
            }
        }
    }
}
