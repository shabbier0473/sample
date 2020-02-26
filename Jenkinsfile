pipeline{
    agent any 
    parameters{
        gitParameter branchFilter: 'origin/(.*)', defaultValue: 'origin/master', name: 'BRANCH', type: 'PT_BRANCH'
        gitParameter name: 'TAG',type: 'PT_TAG', defaultValue: 'master'
    }
    stages{
        stage ('master') {
            when { 
                expression {GIT_BRANCH == 'origin/master'  }
            }
            tools { maven 'MAVEN_HOME'
            steps{
                echo "master"
            }
        }
        stage ('release'){
            when {
                expression {GIT_BRANCH == 'origin/release'  }
            }
            tools { maven 'MAVEN_HOME' }
            steps{
                    echo 'release'
            }
        }
    }
}
