pipeline{
    agent any
    stages{
        stage('SonarQube analysis'){
            tools{
                SonarQube Scanner 'SONAR_RUNNER_HOME'
            }
            steps{
                sh '${SONAR_RUNNER_HOME}/sonar-scanner'
            }
        }
    }
}
