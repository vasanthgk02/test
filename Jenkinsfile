properties([githubProjectProperty(displayName: '', projectUrlStr: 'https://vasanthgk02-admin@bitbucket.org/vasanthgk02/test.git/')])
pipeline {
    
    agent any
    triggers {
        githubPullRequest(
            branches: [[compare: 'test:develop'], [compare: 'test:release']]
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
