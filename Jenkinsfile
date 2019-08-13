pipeline 
{
agent any
    stages
    {
      stage('S3download') 
        {      
            steps {
                withAWS(region:'us-east-2',credentials:'aws-static')\
                {
                    s3Download(file: 'index.html', bucket: 'jenkins-udacity', path: '')
                }
            }
        }
    }
}
