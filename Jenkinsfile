pipeline {
  agent any
  tools { 
        maven 'Maven_3_5_2'  
    }
   stages{
    stage('CompileandRunSonarAnalysis') {
            steps {	
		sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=cicdprojectnew -Dsonar.organization=cicdproject -Dsonar.host.url=https://sonarcloud.io -Dsonar.login=bafa3982c68f390a66ee9e1630c10ecbcbbeea8e'
			}
        } 
   stage('RunSCAAnalysisUsingSnyk') {
            steps {		
				withCredentials([string(credentialsId: 'snyk', variable: 'snyk')]) {
					sh 'mvn snyk:test -fn'
				}
			}
    }		
  }
}

