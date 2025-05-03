pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
  environment {
        SONAR_TOKEN = credentials('SONAR_TOKEN')
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=buggywebapps -Dsonar.organization=buggywebapps -Dsonar.host.url=https://sonarcloud.io -Dsonar.token=$SONAR_TOKEN'
			}
        } 
  }
}
