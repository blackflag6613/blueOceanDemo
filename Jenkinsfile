pipeline {
  agent any
  stages {
    stage('checkout_git') {
      steps {
        git(url: 'https://github.com/elestopadov/jenkins-example-app.git', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy_to_Dev_1') {
      parallel {
        stage('Deploy_to_Dev_1') {
          steps {
            sleep 10
            echo 'This is deploy to server1'
          }
        }

        stage('Deploy_to_Dev2') {
          steps {
            sleep 35
            echo 'This is deploy to server1'
          }
        }

      }
    }

    stage('Test') {
      steps {
        echo 'Testing ....'
      }
    }

  }
}