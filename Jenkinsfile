pipeline{
    agent any
      stages {
         stage('git checkout'){
              steps{ 
                script{
                git credentialsId: 'd407d89a-7cfe-47ce-883c-385bc6217308', url: 'https://github.com/bisthan/spring-boot-mongo-docker.git' 
              }
                  }
         }
         stage('build the package with maven'){
            steps{
              script{
              sh 'mvn clean package'
              }
             }
         }
         stage('docker build'){
            steps{
                script{
                    sh 'docker build -t spring_boot .'
                    
                }
            }
         }
      }
}