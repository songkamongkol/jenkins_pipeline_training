pipeline {
  agent {
    label 'jdk8'
  }
  stages {
    stage('Say Hi') {
      steps {
        echo "Hi World ${MY_NAME}!"
        sh 'java -version'
        echo "${TEST_USER_USR}"
        echo "${TEST_USER_PSW}"
      }
    }
  }
  environment {
    MY_NAME = 'Boon'
    TEST_USER = credentials('test-user')
  }
  parameters {
    string(name: 'Name', defaultValue: 'whoever you are', description: 'Who should I say hi to?')
  }
}