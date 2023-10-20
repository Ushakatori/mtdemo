node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'Sonarscanner';
    withSonarQubeEnv() {
     sh "mvn clean verify sonar:sonar"
    }
  }
}
