pipeline {
  agent any
  stages {
    stage('init') {
      steps {
        echo 'hola mundo'
      }
    }
    stage('build'){
       when {
                expression { BRANCH_NAME ==~ /(release.*)/ }
       }
      steps{
      bat 'mvn clean install'
        mail bcc: '', body: 'Se ha generado un despliegue de una rama BRANCH_NAME', cc: '', from: '', replyTo: '', subject: 'branch desplegado', to: 'wcvaler@pe.ibm.com'
      }
    }
  }
}
