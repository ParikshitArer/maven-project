pipeline{

agent{

label 'server-1'

}

tools{
    maven 'Maven'
}


stages
{

stage('Build'){
    steps{
        sh 'mvn clean package'
    }

    post{
        success{
            archiveArtifacts artifacts: '**/target/*.war', fingerprint: true
        }
    }







}




}
}