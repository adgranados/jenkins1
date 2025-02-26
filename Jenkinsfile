import groovy.json.JsonSlurperClassic

def jsonParse(def json){
  new groovy.json.JsonSlurperClassic().parseText(json)
}

pipeline { 
  agent { label 'master'}
  environment {
    appName ="variable"
  }
  stages{
    stage("Stage 1"){
      steps {
        script {
          sh "echo 'hola mundo'"
        }
      }
    }
  }
  post {
    always{
      deleteDir()
        sh "echo 'fase always'"
    }
    success {
        sh "echo 'fase Success'"
    }
    failure {
        sh "echo 'fase Success'"
    }
  }
}
