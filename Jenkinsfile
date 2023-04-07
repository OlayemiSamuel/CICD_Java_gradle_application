pipeline {
    agent any
    
    stages {
        stage("sonar quality check"){
            agent {
                docker {
                    image 'openjdk:11'
                }
            }
            steps {
                script {
                
                    echo "This was changed!!!!!!!!!!!!!!#######################################"
                    
                    withSonarQubeEnv(credentialsId: 'sonar-token') {
                        sh 'chmod +x gradlew'
                        sh './gradlew sonarqube'
                    }
                    
                    
                }
            }
        
        }
        
    }

}

