pipeline {
    agent any
    stages {
      stage('Build') {
         steps {
           sh 'docker build -t kibana:5.3.2 .'
         }
      }
      stage('Push to registry') {
         steps {
           sh 'docker login -u mniass -p 17decembre'
           sh 'docker tag kibana:5.3.2 mniass/kibana:5.3.2'
           sh 'docker push  mniass/kibana:5.3.2'
         }
      }
    } 
}
