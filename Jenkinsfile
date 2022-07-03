pipeline{
    agent any

    stages{
        stage('Build'){
            steps{
                sh 'mvn clean install -DskipTests'
            }
        }post{
            success{
                archiveArtifacts artifacts: '**/target/*.war'
            }
        }

    }
}