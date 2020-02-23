pipeline{
    agent any
    stages{
        stage ('sonar'){
            tools{
                sonar 'sonar'
            }
            steps{
                sh '${SONAR_RUNNER_HOME}/sonar-scanner'
            }
        }
    }
}
