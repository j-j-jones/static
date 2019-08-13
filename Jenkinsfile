pipeline {
    agent any
    options {
	withAWS(profile:'myProfile')
    s3Upload(file:'index.html', bucket:'jenkins-udacity')
}
    stages {
        stage('Build') {
            steps {
              sh 'echo "Hello World!"'
              sh '''
                  echo "Multiline shell steps work too"
                  ls -lah
                 ''' 
            }
        }
    }
}
