pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh '''./mvnw clean compile
'''
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.projectName=\'Petclinic\' \\
  -Dsonar.host.url=http://15.206.207.34:9000 \\
  -Dsonar.token=sqp_109aacdd201cf0011f2b09f479d76a512d87e921'''
      }
    }

  }
}