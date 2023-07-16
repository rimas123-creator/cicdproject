pipeline {
  agent any
   stages{
    stage('Build and Analyze') {
            steps {
                // Run the SonarScanner analysis
                withSonarQubeEnv('SonarCloud') {
                    sh 'mvn clean verify sonar:sonar -Dsonar.projectKey=cicdproject'
                }
            }
  }
}
}
