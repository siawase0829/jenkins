pipeline {
  agent any
  stages {
    stage('step1') {
      steps {
        echo 'Hell'
      }
    }

    stage('step2') {
      parallel {
        stage('step2') {
          steps {
            build 'job-test1'
            
          }
        }

        stage('') {
          steps {
            sh '''echo "Hello world"
echo "Hello world2"
ls -al'''
          }
        }

      }
    }

  }
  environment {
    CC = 'lang'
  }
}
