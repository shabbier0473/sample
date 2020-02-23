pipeline{
    agent any
    stages{
        stage ('sonarqube analysis'){
            def scannerHome = tool 'SonarScanner 4.2';
            withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
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
