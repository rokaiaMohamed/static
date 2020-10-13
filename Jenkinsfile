pipeline {
     agent any
     stages {
         stage ('Upload to AWS') {
             steps {
                 sh 'echo "Hello World with AWS cred"'
                 withAWS(credentials:'AKIA2Q7JFDZOASPHOKEP') {
                   s3Upload(file:'index.html', bucket:'jenkines-pipeline', path:'index.html')
                 }
                 
             }
         }
     }
} 
