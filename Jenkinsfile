}

node {
  stage('SCM') {
    git 'https://github.com/NishantSharma91/Squaretrade.git'
  }
  stage('SonarQube analysis') {
    withSonarQubeEnv() { // Will pick the global server connection you have configured
      sh './gradlew sonarqube'
    }
  }
}
