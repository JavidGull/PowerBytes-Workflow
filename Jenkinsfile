pipeline {
    agent none
    stages {
        stage(‘build’) {
          agent {
            label "Develop"
           }
           steps {
             sh 'echo test for develop branch' 
            }
        }
     }
}
