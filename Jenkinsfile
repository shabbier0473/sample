pipeline{
    agent any
    stages{
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
