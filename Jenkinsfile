pipeline {
     agent any
     stages {
         stage ('build') {
             steps {
                 sh 'echo "Hello World"'
                 sh '''
                     echo "Multiline steps works too"
                     ls -lah
                 '''
             }
         }
     }
} 
