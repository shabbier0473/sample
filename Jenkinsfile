pipeline{
    agent any
    stages{
        stage ('sonarqube analysis'){
            tools{
                sonar 'SONAR_RUNNER_HOME'
                withSonarQubeEnv('sonar')
                sh "${scannerHome}/bin/sonar-scanner"
        }
        stage ('build'){
            tools{
                maven 'MAVEN_HOME'
            }
            steps{
                sh 'mvn --version'
                sh 'mvn install'
            }
        }
    }
}
