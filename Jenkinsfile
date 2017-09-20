pipeline {
  agent any
  stages {
    stage('Intro') {
      steps {
        echo "Hello World!"
      }
    }
    stage('Input') {
      steps {
        input(message: 'User input required', ok: 'Engage!',
          parameters: [
            choice(name: 'BRANCH', description: 'Branch', choices: 'master\ndevelop')
            credentials(name: 'CREDENTIAL', description: 'Credential', credentialType: "Username with password", required: true)
          ]
        )
      }
    }
    stage('Outro') {
      steps {
        echo "Goodbye World!"
      }
    }
  }
}
