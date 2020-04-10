pipeline{
    agent any
    stages{
        stage('Upload to AWS'){
            steps{
                withAWS(region: 'ap-south-1' , credentials: 'aws-static'){
                    sh 'echo "Upload to the AWS Bucket"'
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'udacity-devopsnd-p3')
                }
            }
        }
    }
}
