pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        echo 'hola mundo'
      }
    }
    stage('build'){
      steps{
      bat 'mvn clean install'
        mail bcc: '', body: 'Se ha generado un despliegue de una rama', cc: '', from: '', replyTo: '', subject: 'branch desplegado', to: 'wcvaler@pe.ibm.com'
      }
    }
  }
}
