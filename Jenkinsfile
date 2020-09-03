pipeline {
  agent {
    kubernetes {
      	cloud 'kubernetes'
      	defaultContainer 'jnlp'
      }
    }
  stages {
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "mysql-deployment.yml", kubeconfigId: "MINIKUBECONFIG")
        }
      }
    }
  }
}