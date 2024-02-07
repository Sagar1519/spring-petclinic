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
        sh '''mvn   sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
 
  -Dsonar.host.url=http://localhost:9000 \\
  -Dsonar.login=sqp_109aacdd201cf0011f2b09f479d76a512d87e921'''
      }
    }

  }
}