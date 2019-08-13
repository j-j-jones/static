pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Helo World!!'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                withAWS(region:'us-east-2',credentials:'aws-static')
                {
                    s3Upload(file: 'index.html', bucket: 'jenkins-udacity', path: '')
                }
            }
        }
    }
}
