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
            steps{
                sh 'cd ..'
                sh 'cd sample'
                echo "========master======="
                sh 'mvn install'
            }
        }
        stage ('release'){
            when {
                expression {GIT_BRANCH == 'origin/release'  }
            }
            steps{
                 sh 'mvn --version' 
                 echo '========release=========='
            }
        }
    }
}
