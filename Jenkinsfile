pipeline {
  agent any
  stages {
    stage('Welcome') {
      steps {
        echo 'Welcome to pipeline through BlueOcean'
      }
    }

    stage('Connect to SCM') {
      steps {
        git(url: 'https://github.com/pavansw/ab-inbevDevops.git', branch: 'master', changelog: true, poll: true)
      }
    }

    stage('Run Python Application') {
      steps {
        sh 'python hello.py'
      }
    }

    stage('Final') {
      steps {
        echo 'Pipeline Successsssss'
      }
    }

  }
}