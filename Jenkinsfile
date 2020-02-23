pipeline{
    agent any
    stages{
        stage('SonarQube analysis'){
           steps{
               sh'mvn clean' 
               sh'${SONAR_RUNNER_HOME}/sonar-scanner'
            }
        }
    }
}
