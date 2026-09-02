pipeline{

agent{

label 'server-1'

}

environment{

NAME = "Parikshit"

}

tools{
    maven 'Maven'

}


stages
{

stage('Build'){
    steps{
        sh 'mvn clean package'

        echo "Hello my name is $NAME "
    }

    post{
        success{
            archiveArtifacts artifacts: '**/target/*.war', fingerprint: true
        }
    }







}




}
}