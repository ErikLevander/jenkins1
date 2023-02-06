pipeline {
  agent any
  stages {
    stage('install') {
      parallel {
        stage('install') {
          steps {
            sh 'pip install autopep8 pylint'
          }
        }

        stage('req') {
          steps {
            sh 'python3 -m pip install -r requirements '
          }
        }

      }
    }

    stage('autopep') {
      parallel {
        stage('autopep') {
          steps {
            sh 'python3 -m autopep8 --diff ./src/main.py'
          }
        }

        stage('pylint') {
          steps {
            sh 'python3 -m pylint --disable=C0304 ./src/'
          }
        }

      }
    }

  }
}