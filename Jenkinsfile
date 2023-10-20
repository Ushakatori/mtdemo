node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'sonarscanner';
    withSonarQubeEnv() {
     sh "mvn clean verify sonar:sonar"
    }
  }
}
