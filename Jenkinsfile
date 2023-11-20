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
      when {
        expression { branchName == 'test' && (pullRequest != null && pullRequest.originBranch == 'test' && pullRequest.targetBranch == 'develop') || (pullRequest != null && pullRequest.originBranch == 'test' && pullRequest.targetBranch == 'release') }
      }
      steps {
        checkout scm
        sh 'echo Hi'
      }
    }
  }
}
