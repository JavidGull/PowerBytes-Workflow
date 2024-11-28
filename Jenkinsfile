pipeline {
    agent none
    stages {
        stage('Deploy') {
          agent {
            label "Jenkins_Production"
          }
          steps {
            sh '''  
              sudo docker stop apache_ubuntu 
              sudo docker rm $(sudo docker ps -a --filter "name=^apache_ubuntu" --format "{{.ID}}")
              sudo docker build . -t pb_workflow_image
              sudo docker run --name apache_ubuntu -p 82:80 -d pb_workflow_image  
            '''
            }
        }
     }
}
