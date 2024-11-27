pipeline {
    agent none
    stages {
        stage('Deploy') {
          agent {
            label "Production"
           }
           steps {
             sh 'sudo docker build dockerfile -t pb_workflow_image'
             sh 'sudo docker run --name apache_ubuntu -p 82:80 -d PB_WorkfLow_image'                          
            }
        }
     }
}
