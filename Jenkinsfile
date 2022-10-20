pipeline {
  agent any
  stages {
    stage('hello') {
      parallel {
        stage('hello') {
          steps {
            echo 'hello'
          }
        }

        stage('Compile') {
          steps {
            sh './gradlew compileJava'
          }
        }

      }
    }

    stage('Unit test') {
      steps {
        sh './gradlew test'
      }
    }

  }
}