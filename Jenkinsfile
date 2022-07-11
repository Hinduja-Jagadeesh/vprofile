node{
    stage('build'){
        sh 'make'
        archiveArtifacts artifacts: '**/target/*.war' fingerprint:true
    }
    
    
}
