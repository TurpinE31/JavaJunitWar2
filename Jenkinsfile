pipeline {
  agent any
  stages {
    stage('prepare') {
      agent any
      steps {
        git(url: 'https://github.com/TurpinE31/JavaJunitWar2.git', branch: 'master')
      }
    }

    stage('build') {
      agent any
      steps {
        sh 'mvn clean install'
      }
    }

    stage('test') {
      agent any
      steps {
        junit 'JavaJunitWar/target/surefire-reports/TEST-*.xml'
      }
    }

    stage('deploy') {
      agent any
      steps {
        sh 'echo "deploy"'
      }
    }

  }
}