pipeline {
agent any
stages {
    stage('Deploy') {
      steps {
    withAWS(credentials:'awscredentials') {
        s3Download(file: 'index.html', bucket: 'jenkins-udacity', path: '/home/ubuntu/')
      }
    }
    }
}
}
