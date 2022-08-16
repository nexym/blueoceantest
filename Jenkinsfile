pipeline {
  agent any
  stages {
    stage('developpement') {
      steps {
        echo 'dev test'
      }
    }

    stage('In progress') {
      parallel {
        stage('In progress 1.1') {
          steps {
            echo 'this is the progress step'
          }
        }

        stage('in progress 1.0') {
          steps {
            echo '1 prog'
          }
        }

      }
    }

    stage('Production') {
      steps {
        input(message: 'Are you sure for deploy', ok: 'Yes im sure')
        echo 'Good luck in deploy'
      }
    }

  }
}