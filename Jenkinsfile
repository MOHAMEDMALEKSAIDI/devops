pipeline {
  agent any
  stages {
    stage('verifier mvn') {
      parallel {
        stage('verifier mvn') {
          steps {
            sh '''mvn --version
git --version
java -version'''
          }
        }

        stage('check pom') {
          steps {
            fileExists 'pom.xml'
          }
        }

      }
    }

    stage('ok') {
      steps {
        writeFile(file: 'status', text: 'good', encoding: 'txt')
      }
    }

  }
}