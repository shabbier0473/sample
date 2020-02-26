pipeline{
    agent any 
    parameters{
        gitParameter branchFilter: 'origin/(.*)', defaultValue: 'origin/master', name: 'BRANCH', type: 'PT_BRANCH'
    }
    stages{
        stage (master) {
            when { 
                expression {GIT_BRANCH == 'origin/master'  }
            }
            steps{
                echo "master"
            }
        }
        stage ('release'){
            steps{
                    echo 'release' }
        }
    }
}
