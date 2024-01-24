node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarTest';
    withSonarQubeEnv() {
      println ${env.SONAR_HOST_URL}
      bat "%scannerHome%/bin/sonar-scanner"
    }
  }
}
