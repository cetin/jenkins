pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
        stage('run-parallel-branches') {
              steps {
                parallel(
                  a: {
                    echo "This is branch a"
                  },
                  b: {
                    echo "This is branch b"
                  }
                )
              }
            }
    }
}
