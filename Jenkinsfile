pipeline {
	agent any
	  tools{
        jdk 'java11'
        maven 'maven3'
        // sonarqube scanner 'sonarqube'
    }
    stages {
      stage('SonarQube Analysis') {
        steps{  // def mvn = tool 'Default Maven';
          withSonarQubeEnv('sonarqube') {
            sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=hello_world_pipeline -Dsonar.projectName='hello_world_pipeline'"
         }
       }
     }
  }
}
  
