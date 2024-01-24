node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    withSonarQubeEnv() {
      def sonarRunner = tool name: 'SonarTest', type: 'hudson.plugins.sonar.SonarRunnerInstallation'
      bat "echo %SONAR_HOST_URL%"
      bat "%sonarRunner%\\bin\\sonar-scanner.bat"
    }
  }
}
