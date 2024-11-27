pipeline {
    agent none
    stages {
        stage(‘Deploy’) {
          agent {
            label "Production"
           }
           steps {
             sh '''
              docker build dockerfile -t PB_WorkfLow_image
              docker run --name apache_ubuntu -p 82:80 -d PB_WorkfLow_image
             '''               
            }
        }
     }
}
