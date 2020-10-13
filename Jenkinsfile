pipeline {
     agent any
     stages {
         stage ('Lint HTML') {
             steps {
                 sh 'tidy -q -e *.html'                 
             }
         }
         stage ('Upload to AWS') {
             steps {
                 sh 'echo "Hello World with AWS cred"'
                 withAWS(credentials:'aws-static') {
                   s3Upload(file:'index.html', bucket:'jenkines-pipeline', path:'index.html')
                 }
                 
             }
         } 
     }
} 
