node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarQubeScanner';
    withSonarQubeEnv() {
     sh "mvn clean verify sonar:sonar"
    }
  }
}
