pipeline{
    agent any 
    environment {
        PATH= "/usr/bin:$PATH"
    }
    
    stages{
        stage("sonar quality check"){
            steps{
                script{
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                            sh 'mvn clean verify sonar:sonar'
                    }

                }  
            }
        }

    }
}
