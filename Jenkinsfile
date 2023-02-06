pipeline {
  agent any
  stages {
    stage('install') {
      steps {
        sh 'pip install autopep8'
      }
    }

    stage('') {
      steps {
        sh 'python3 -m autopep8 --diff ./src/main.py'
      }
    }

  }
}