pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=dsobuggykey -Dsonar.organization=dsobuggykey -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=bafa3982c68f390a66ee9e1630c10ecbcbbeea8e'
			}
        } 
  }
}
}
