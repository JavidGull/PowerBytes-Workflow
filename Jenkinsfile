pipeline {
    agent none
    stages {
        stage(‘git’) {
          agent {
            label "Built-In"
           }
           steps {
             script {
                git 'https://github.com/JavidGull/devop_capstone_project02.git'
              }    
            }
        }
     }
}
