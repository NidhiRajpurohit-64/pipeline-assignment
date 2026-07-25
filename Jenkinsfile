pipeline {
  agent any
  parameters {
    name: 'ENVIRONMENT'
    choices: ['staging','production']
    description: 'Choose deployment environment'
  }
  stages {
    stage('Build') {
      steps {
        echo 'Building the application...'
      }
    }
    stage('Test') {
      steps {
        echo 'Running tests...'
      }
    }
    stage('Deploy') {
      steps {
        echo "Deploying to ${params.ENVIRONMENT}"
      }
    }
  }
  post {
    success {
      echo 'Pipeline completed successfully!'
    }
    failure {
      echo 'Pipeline failed!'
    }
  }
}
