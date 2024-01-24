node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = "D:\\sonarqube-10.3\\sonar-scanner-cli-5.0.1.3006-windows"
    withSonarQubeEnv() {
      bat "echo %SONAR_HOST_URL%"
      bat "%scannerHome%\\bin\\sonar-scanner.bat"
    }
  }
}
