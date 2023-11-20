properties([
    githubProjectProperty(displayName: '', projectUrlStr: 'https://github.com/vasanthgk02/test.git/'), 
    pipelineTriggers([
        githubPush()
    ])
])
pipeline {
    
    agent any

    
   stages {
    stage('Pull Request Build') {
      // when {
      //   expression { branchName == 'test' && (pullRequest != null && pullRequest.originBranch == 'test' && pullRequest.targetBranch == 'develop') || (pullRequest != null && pullRequest.originBranch == 'test' && pullRequest.targetBranch == 'release') }
      // }
        when {
                expression {
                    // Only trigger if the pull request is from the test branch to either develop or release branch
                    return env.CHANGE_TARGET ==~ /(origin\/develop|origin\/release)/ && env.CHANGE_BRANCH == 'origin/test'
                }
            }
      steps {
        checkout scm
        sh 'echo Hi'
      }
    }
  }
}
