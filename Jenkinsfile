node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner1';
    withSonarQubeEnv() {
     sh "${mvn}/bin/mvn clean verify sonar:sonar"
    }
  }
}
