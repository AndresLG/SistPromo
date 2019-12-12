pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean package'
      }
    }

    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }

    stage('Deploy') {
      steps {
        sh '/root/.jenkins/workspace/SistPromo_master/target/SistPromo.war /opt/wildfly/standalone/deployments'
      }
    }

  }
}