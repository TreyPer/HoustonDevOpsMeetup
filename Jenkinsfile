pipeline {
  agent none
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sleep 5
          }
        }
        stage('Build Env 2') {
          steps {
            sleep 3
          }
        }
      }
    }
    stage('Unit Test') {
      parallel {
        stage('Unit Test') {
          steps {
            sleep 5
          }
        }
        stage('Windows') {
          steps {
            echo 'hello World'
          }
        }
        stage('LInux') {
          steps {
            echo 'hello world'
          }
        }
      }
    }
    stage('Approval Step') {
      steps {
        input(message: 'Do approve this?', id: 'Is it ok? ', ok: 'Yes approve')
      }
    }
    stage('Deploy') {
      steps {
        sleep 5
      }
    }
  }
}
