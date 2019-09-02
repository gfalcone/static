pipeline {
     agent any
     stages {
         stage('Build') {
             withAWS(credentials:'aws-static', region:'us-west-2') {
	         s3Upload(file:'index.html', bucket:'static-bucket-paolo', path:'index.html')
             }
         }
     }
}
