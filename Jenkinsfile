node {
  stage('SCM') {
    git 'https://github.com/NishantSharma91/Squaretrade.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'SonarScanner 4.0';
    withSonarQubeEnv('Sonarscannertest') { // If you have configured more than one global server connection, you can specify its name
      bat "${scannerHome}/bin/sonar-scanner"
    }
  }
}
