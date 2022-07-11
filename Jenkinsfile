pipeline{
    agent any

    stages {
        stage('Build Stage') {
            steps {
                sh 'mvn clean install -DskipTests'

            }


                        }

    }post{
        success{
            sh 'echo good work'
        }
        
    }
    

}
