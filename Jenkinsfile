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
        steps {
            print env
            script {
                    def sourceBranch = env.CHANGE_BRANCH
                    def targetBranch = env.CHANGE_TARGET

                    echo "Source Branch: ${sourceBranch}"
                    echo "Target Branch: ${targetBranch}"

                    if (sourceBranch == 'test' && (targetBranch == 'develop' || targetBranch == 'release')) {
                        echo "PR is from 'test' to '${targetBranch}'. Triggering the build..."
                    } else {
                        echo "PR is not from 'test' to 'develop' or 'release'. Skipping the build."
                    }
            }
        }
    }
  }
}
