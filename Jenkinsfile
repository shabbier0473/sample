pipeline{
    agent any
    stages{
        stage('SonarQube analysis'){
           steps{
                sh '${SONAR_RUNNER_HOME}/sonar-scanner'
            }
        }
    }
}
