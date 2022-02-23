pipeline {
  agent any
  stages {
    stage('compile-app') {
      steps {
        echo 'this is the comile job'
        sh 'npm install'
      }
    }

    stage('test-app') {
      steps {
        echo 'this is the testjob'
        sh 'npm test'
      }
    }

    stage('package-app') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('archive-app') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'I know how to create pipeline'
    }

  }
}