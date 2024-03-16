pipeline {
    agent {
        node{
            label 'maven'
        }
    environment {
        PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
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
}
  

    

   



