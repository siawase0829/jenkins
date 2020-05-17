pipeline {
  agent any
  stages {
    stage('step1') {
      steps {
        sh '''echo "Hello zzzzzzzzzzzzzzzzzzzzzz" '''
      }
    }

    stage('step2') {
      parallel {
        stage('step2') {
          steps {
            build job:'job-test1', parameters: [[$class: 'LabelParameterValue',name: 'NODE',label:'master']]
            
          }
        }

        stage('step3') {
          steps {
            sh '''echo "Hello world"
echo "Hello world2"
pwd
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
