node {
  stage('SCM') {
    git 'https://github.com/foo/bar.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('My SonarQube Server') { // If you have configured more than one global server connection, you can specify its name
      bat "${scannerHome}/bin/sonar-scanner"
    }
  }
}
