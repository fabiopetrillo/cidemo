pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        parallel(
          "Compile": {
            sh './gradlew compileJava'
            
          },
          "Test": {
            sh './gradlew test'
            
          }
        )
      }
    }
    stage('Build') {
      steps {
        sh './gradlew build'
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deploy in Staging'
      }
    }
  }
}