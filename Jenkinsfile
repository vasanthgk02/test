properties([
    githubProjectProperty(displayName: '', projectUrlStr: 'https://github.com/vasanthgk02/test.git/'), 
    pipelineTriggers([
        githubPullRequests(
            branches: [
                [pattern: 'develop:test'],
                [pattern: 'release:test']
            ]
        ),
        githubPush()
    ])
])
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
