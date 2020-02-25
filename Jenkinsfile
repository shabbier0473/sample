pipeline{
    agent any
    stages{
        stage ('master'){
            when {
                branch 'master'
            }
            tools{
                maven 'MAVEN_HOME'
                jdk 'JAVA_HOME'
            }
            steps{
                timestamps{
                 echo '========master======='
                 sh 'mvn install' 
                }
               
            }
        }
        stage{
            steps{
                echo "shabbir"
            }
        }
        stage ('build release'){
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

