pipeline {
     agent any
     stages {
         stage('Lint HTML') {
             steps {
                 tidy -q -e *.html
             }
         }
         stage('Upload to AWS') {
             steps {
	         withAWS(credentials:'aws-static', region:'us-west-2') {
                      s3Upload(file:'index.html', bucket:'static-bucket-paolo', path:'index.html')
                 }
	     }
         }
     }
}
