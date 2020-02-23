pipeline{
    agent any
    stages{
        stage('SonarQube analysis'){
            tools{
                sonarqube scanner 'SONAR_RUNNER_HOME'
            }
            steps{
                sh '${SONAR_RUNNER_HOME}/sonar-scanner'
            }
        }
    }
}
