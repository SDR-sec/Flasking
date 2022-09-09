pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('Git') {
      steps {
        git(url: 'https://github.com/SDR-sec/Flasking', branch: 'main')
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -t sdrdocker334/flask_app .'
      }
    }

    stage('Docker Login') {
      steps {
        sh 'docker login -u sdrdocker334 -p dckr_pat_9pOV7ksTNfS_2a6zx9Br1ogL9a8'
      }
    }

    stage('Docker Push') {
      steps {
        sh 'docker push sdrdocker334/flask_app'
      }
    }

  }
}