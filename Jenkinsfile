pipeline{
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean install -DskipTests'

            }


        }post{
            success{
                archiveArtifcats artifacts: '**/target/*.war'
            }
        }
        stage('Test'){
            steps{
                sh 'mvn test'
            }
        }

    }

}