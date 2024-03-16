pipeline {
    agent {
        node{
            label 'maven'
        }
    }
    }
    stage('SonarQube analysis') {
    environment {
    scannerHome = tool 'isha-sonar-scanner';
    }
    steps{
    withSonarQubeEnv('isha-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
    }
  }

    

   



