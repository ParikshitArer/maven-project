pipeline{

agent{

label 'server-'

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