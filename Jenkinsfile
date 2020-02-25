pipeline{
    agent any
    stages{
        stage ('master'){
            when {
                branch 'master'
            }
            tools{
                maven 'MAVEN_HOME' }
            steps{
                timestamps{
                 echo '========master======='
                 sh 'mvn install'
                 echo '=====master'
                 sh 'mkdir $branch'
                }
            }
        }
        stage ('shabbir'){
            steps{
                echo "shabbir"
            }
        }
        stage ('release'){
            when {
                branch 'release'
            }
            tools{
                maven 'MAVEN_HOME'
            }
            steps{
                echo '======release========='
                sh 'mvn install'
            }
        }
        stage ('tag build'){
            when {
                buildingTag()
            }
            tools{
                maven 'MAVEN_HOME'
            }

            steps{
                sh 'mvn test'
                echo "=====tag building===="
            }
        }
    }
}

