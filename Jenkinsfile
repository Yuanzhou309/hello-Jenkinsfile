pipeline {
    agent any

    stages {
       
      stage('Upload to AWS') {
              steps {
                  withAWS(region:'ap-southeast-2',credentials:'kevin-aws-jenkins-cred') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index1.html', bucket:'mysamplebucket309')
                  }
              }
         }
        
        
        
    }
}
