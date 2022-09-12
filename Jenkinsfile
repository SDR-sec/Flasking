pipeline {
<<<<<<< HEAD
    enviroment{
        registry = 'sdrdocker334/flask_app'
        registryCredentials = 'docker'
        cluster_name = 'skillstorm'
        namepace = 'sdrkube'
    }
=======
>>>>>>> ee092bbc341d81d9665af5d6976e39dce6d45795
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

<<<<<<< HEAD
stage('Build Stage'){
        steps{
            script{
                dockerImage = docker.build(registry)
            }
        }
}
stage('Deploy Stage'){
    steps {
        script{
            docker.withRegistry('', registryCredentials)
                dockerImage.push()
        }
    }
}

=======
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
>>>>>>> ee092bbc341d81d9665af5d6976e39dce6d45795
