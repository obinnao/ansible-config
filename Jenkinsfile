pipeline {
    agent any

stages {
  stage("Initial cleanup") {
        steps {
          dir("${WORKSPACE}") {
            deleteDir()
          }
         }
      }

  stages {
    stage('Build') {
      steps {
        script {
          sh 'echo "Building Stage"'
        }
      }
    }

    stage('Test') {
      steps {
        script {
          sh 'echo "Testing Stage"'
        }
      }
    }

    stage('Package'){
      steps {
        script {
          sh 'echo "Packaging App" '
        }
      } 
    }

    stage('Deploy')
      steps {
        script {
          sh 'echo "Deploying to Dev"'
        }
      }

    stage("clean up")
      steps {
       cleanWs()
  
     }
    }
}   

