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
            build job:'job-test1', parameters: [[$class: 'LabelParameterValue',name: 'NODE',label:'master']]
            
          }
        }

        stage('') {
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
