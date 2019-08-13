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
                echo 'Deploying..'
                withAWS(region:'us-east-1',credentials:'aws-static')
                {
                    s3Upload(file: 'index.html', bucket: 'jenkins-udacity', path: '')
                }
            }
        }
    }
}
