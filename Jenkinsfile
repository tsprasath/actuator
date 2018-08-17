pipeline {
  agent {
    docker {
      image 'maven:3-alpine'
      args '-v $HOME/.m2:/root/.m2'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''mvn -B -DskipTests clean package'''
      }
    }
  }
  environment {
    Name = 'testing'
  }
}
