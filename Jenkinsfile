pipeline {
    agent any
      stages {
        stage('Build') {
            steps {
              sh 'echo "Hello World!"'
              sh '''
                  echo "Multiline shell steps work too"
                  ls -lah
                 ''' 
            }
		
	stage('Deploy') {
            steps {
                withAWS(region:'us-east-2', credentials:'aws-static')
    s3Upload(file:'index.html', bucket:'jenkins-udacity')
            }
        }	
	
        }
    }
}
