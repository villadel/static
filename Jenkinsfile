pipeline{
    agent any
    stages{
       stage('Upload to AWS') {
              steps {
                  withAWS(region:'us-east-2',credentials:'aws-jenkins') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkins-static-project')
                
              }
         }
    }
    }

    post{
      
        success{
            echo "========pipeline executed successfully ========"
        }
        failure{
            echo "========pipeline execution failed========"
        }
    }
}