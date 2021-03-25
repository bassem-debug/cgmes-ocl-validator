pipeline {
  agent {
    docker {
      image 'centos'
    }

  }
  stages {
    stage('') {
      steps {
        timeout(time: 22, activity: true) {
          sleep 33
        }

        echo 'hi'
      }
    }

  }
}