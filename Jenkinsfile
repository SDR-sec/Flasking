pipeline {
    enviroment{
        registry = 'sdrdocker334/flask_app'
        registryCredentials = 'docker'
        cluster_name = 'skillstorm'
        namepace = 'sdrkube'
    }
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
  }
}