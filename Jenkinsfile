pipeline{
    agent any
    environment{

    }
    stages{
        stage(Checkout){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Hinduja-Jagadeesh/vprofile.git']]])
            }
        }
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