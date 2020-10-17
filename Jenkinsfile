pipeline {
    agent any

    tools {
      maven 'Maven3.6.3'
    }

    stages {
        stage('build') {
            steps {
                echo 'This is build job'
                sh 'mvn compile'
            }
            }

        stage('test') {
            steps {
                echo 'This is test job'
                sh 'mvn clean test'
            }
        }
        stage('package') {
            steps {
                echo 'This is package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    post{
        always{
             echo 'this pipeline has completed....'
        } 
    }
}
