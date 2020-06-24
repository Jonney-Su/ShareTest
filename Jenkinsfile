pipeline {
  agent any
  stages {
    stage('Hello') {
      steps {
        echo 'Hello World'
      }
    }

    stage('Example') {
      input {
        message 'Should we continue?'
        id 'Yes, we should.'
        submitter 'alice,bob'
        parameters {
          string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        }
      }
      steps {
        echo "Hello, ${PERSON}, nice to meet you."
      }
    }

    stage('s3') {
      steps {
        input(message: 'm1', id: 'id1', ok: 'ok1')
      }
    }

  }
}