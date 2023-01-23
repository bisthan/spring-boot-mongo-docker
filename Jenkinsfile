pipeline{

    agent any

      stages{
         stage("git checkout"){
              steps { 
                git credentialsId: 'd407d89a-7cfe-47ce-883c-385bc6217308', url: 'https://github.com/bisthan/spring-boot-mongo-docker.git' 
                  }
         }
         stage("build the package with maven"){
            steps {
              def mavenHome = tool name: "maven-3.8.4" , type: "maven"
              def mavenCMD = "${mavenHome}/bin/mvn"
              sh "${mavenCMD} clean package"
             }
         }
      }
}