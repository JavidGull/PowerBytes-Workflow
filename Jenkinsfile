pipeline {
    agent none
    stages {
        stage(‘git’) {
          agent {
            label "localhost"
           }
           steps {
             script {
                git 'https://github.com/JavidGull/devop_capstone_project02.git'
              }    
            }
        }
     }
}

