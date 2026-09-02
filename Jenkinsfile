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

}

stage('Test'){



parallel{

    stage('TestA'){

        steps{
            echo 'This is test A'
        }
    }

    stage('TestB'){

        steps{
            echo 'This is test B'
        }
    }
}
  post{
        success {
            archiveArtifacts artifacts: '**/target/*.jar'
        }
    }
}

}




}





