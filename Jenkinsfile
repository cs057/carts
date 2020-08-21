pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is build job'
        sh 'mvn compile'
      }
    }

    stage('test') {
      steps {
        echo 'this is test job'
        sh 'mvn clean test'
      }
    }

    stage('package') {
      steps {
        echo 'this is package job'
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'Maven 3.6.3'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}