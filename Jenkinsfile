pipeline {
  agent any
  stages {
    stage('compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=spring-petclinic \\
  -Dsonar.host.url=http://13.201.83.250:9000 \\
  -Dsonar.token=sqp_7525f3cc9ddce2ca703b403864ce4099ae96c85e'''
        sh '''mvn clean verify sonar:sonar \\
  -Dsonar.projectKey=spring-petclinic \\
  -Dsonar.host.url=http://13.201.83.250:9000 \\
  -Dsonar.token=sqp_7525f3cc9ddce2ca703b403864ce4099ae96c85e'''
      }
    }

  }
}