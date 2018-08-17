pipeline {
  agent {
    docker {
      image 'maven:latest'
      args '$WORKSPACE:/tmp -u="root" -w /tmp'
    }

  }
  stages {
    stage('build') {
      steps {
        sh '''mvn -v
mvn -B -DskipTests clean package
'''
      }
    }
  }
  environment {
    Name = 'testing'
  }
}