pipeline {
  agent any
  stages {
    stage('step1') {
      steps {
        sh '''echo "Hello zzzzzzzzzzzzzzzzzzzzzz" '''
      }
    }

    stage('平行動作') {
      parallel {
        stage('step１') {
          steps {
            build job:'job-test1', parameters: [[$class: 'LabelParameterValue',name: 'NODE',label:'master']]
            
          }
        }

        stage('step２') {
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
