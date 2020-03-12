pipeline{
    agent { label "maven" }
    tools { maven "MAVEN_HOME" }
    stages{
        stage ("compile"){
            steps{
                sh "mvn compile"
            }
        }
    }
}
