properties([
    githubProjectProperty(displayName: '', projectUrlStr: 'https://github.com/vasanthgk02/test.git/'), 
    pipelineTriggers([
        // githubPush()
    ])
])

pipeline {
    
    agent any   
    stages {
    stage('Pull Request Build') {
        when {
                expression {
                    return env.CHANGE_TARGET ==~ /(develop|release)/ && env.CHANGE_BRANCH == 'test'
                }
        }   
        steps {
            sh 'echo Hi'
            print env
        }
    }
  }
}
