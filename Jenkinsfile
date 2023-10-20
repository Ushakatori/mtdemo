node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner1';
    withSonarQubeEnv() {
     sh "mvn clean verify sonar:sonar"
    }
  }
}
