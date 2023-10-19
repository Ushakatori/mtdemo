node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner1';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner1"
    }
  }
}
